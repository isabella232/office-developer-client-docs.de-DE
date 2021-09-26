---
title: Abrufen des Pfads einer bestimmten Version von MAPI für den Stanard-Mail-Client
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5ee7fb05-cfb3-6b68-5a9a-1d6375f2e879
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 696e1ea9fc3eedbdb8c3e113498d06ad0b7920fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610846"
---
# <a name="get-the-path-of-a-specific-version-of-mapi-for-the-default-mail-client"></a>Abrufen des Pfads einer bestimmten Version von MAPI für den Stanard-Mail-Client

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält ein Codebeispiel in C++, das zeigt, wie sie den Pfad einer bestimmten MapI-Version abrufen, die vom Standard-E-Mail-Client auf einem Computer verwendet wird. MAPI-Mailclients können in der Registrierung eine benutzerdefinierte DLL angeben, an die die MAPI-Stubbibliothek MAPI-Aufrufe laden und verteilen soll. Der Registrierungsschlüssel für diese benutzerdefinierte DLL für einen Standard-E-Mail-Client ist **MSIComponentID** unter dem **HKLM\Software\Clients\Mail-Schlüssel** des Standard-E-Mail-Clients. Die [FGetComponentPath-Funktion,](fgetcomponentpath.md) die von der MAPI-Stubbibliothek mapistub.dll exportiert wird, kann den Pfad zu der benutzerdefinierten Version der MAPI zurückgeben, die durch den **MSIComponentID-Registrierungsschlüssel** angegeben wird. 
  
Dieses Codebeispiel enthält zwei Funktionen:  `HrGetRegMultiSZValueA` und  `GetMAPISVCPath` . Die  `GetMAPISVCPath` Funktion verwendet [FGetComponentPath,](fgetcomponentpath.md) um den Pfad zur benutzerdefinierten Version der MAPI abzurufen. Es wird davon ausgegangen, dass der Standard-E-Mail-Client Microsoft Office Outlook 2007 ist, und übergibt den Wert an **FGetComponentPath,** der `{FF1D0740-D227-11D1-A4B0-006008AF820E}` Outlook 2007 als Komponenten-ID der MAPI für den **MSIComponentID-Registrierungsschlüssel** festlegt. 
  
> [!NOTE]
> In der Praxis sollten Sie nicht davon ausgehen, dass der Wert immer  `{FF1D0740-D227-11D1-A4B0-006008AF820E}` die Komponenten-ID der MAPI ist und direkt an **FGetComponentPath** übergeben. Um zuverlässig herauszufinden, welche Version von MAPI Outlook auf einem Computer verwendet, müssen Sie den Wert von **MSIComponentID** aus der Registrierung lesen und an **FGetComponentPath** übergeben. 
  
In den folgenden Schritten wird beschrieben, wie  `GetMAPISVCPath` dies funktioniert. 
  
1. Lädt die MAPI-Stubbibliothek mapistub.dll aus dem Systemverzeichnis.
    
2. Angenommen, mapistub.dll die **FGetComponentPath-Funktion** exportiert, wird versucht, die Adresse dieser Funktion von mapistub.dll abzurufen. 
    
3. Wenn beim Abrufen der Adresse von mapistub.dll ein Fehler auftritt, wird versucht, die Adresse von mapi32.dll abzurufen.
    
4. If getting the address of **FGetComponentPath** succeeds, it opens the registry and uses the `HrGetRegMultiSZValueA` function to read the registry values under **HKLM\Software\Clients\Mail\Microsoft Outlook**. 
    
5. Ruft **FGetComponentPath mit** Angabe des Werts `{FF1D0740-D227-11D1-A4B0-006008AF820E}` auf, um den Pfad zur mapi-Version abzurufen, die Outlook 2007 verwendet.
    
Beachten Sie, dass zur Unterstützung lokalisierter Kopien von MAPI für englische und nicht englische Gebietsschemas im Codebeispiel die Werte für die **UNTERschlüssel MSIApplicationLCID** und **MSIOfficeLCID** gelesen werden und **FGetComponentPath** aufgerufen wird, zuerst **MSIApplicationLCID** als  *SzQualifier*  angegeben wird und dann erneut **MSIOfficeLCID** als  *szQualifier*  angegeben wird. Weitere Informationen zu Registrierungsschlüsseln für E-Mail-Clients, die nicht englischsprachige Sprachen unterstützen, finden Sie unter [Setting Up the MSI Keys for Your MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).
  
```cpp
// HrGetRegMultiSZValueA 
// Get a REG_MULTI_SZ registry value - allocating memory using new to hold it. 
void HrGetRegMultiSZValueA( 
    IN HKEY hKey, // the key. 
    IN LPCSTR lpszValue, // value name in key. 
    OUT LPVOID* lppData) // where to put the data. 
{ 
    *lppData = NULL; 
    DWORD dwKeyType = NULL;       
    DWORD cb = NULL; 
    LONG lRet = 0; 
    
    // Get its size 
    lRet = RegQueryValueExA( 
        hKey, 
        lpszValue, 
        NULL, 
        &amp;dwKeyType, 
        NULL, 
        &amp;cb); 
 
    if (ERROR_SUCCESS == lRet &amp;&amp; cb &amp;&amp; REG_MULTI_SZ == dwKeyType) 
    { 
        *lppData = new BYTE[cb]; 
       
        if (*lppData) 
        { 
            // Get the current value 
            lRet = RegQueryValueExA( 
                hKey,  
                lpszValue,  
                NULL,  
                &amp;dwKeyType,  
                (unsigned char*)*lppData,  
                &amp;cb); 
          
            if (ERROR_SUCCESS != lRet) 
            { 
                delete[] *lppData; 
                *lppData = NULL; 
            } 
        } 
    } 
} 
 
typedef BOOL (STDAPICALLTYPE FGETCOMPONENTPATH) ( 
    LPSTR szComponent, 
    LPSTR szQualifier, 
    LPSTR szDllPath, 
    DWORD cchBufferSize, 
    BOOL fInstall); 
typedef FGETCOMPONENTPATH FAR * LPFGETCOMPONENTPATH;  
 
/////////////////////////////////////////////////////////////////////////////// 
// Function name   : GetMAPISVCPath 
// Description       : This will get the correct path to the MAPISVC.INF file. 
// Return type      : void  
// Argument         : LPSTR szMAPIDir - Buffer to hold the path to the MAPISVC file. 
//                    ULONG cchMAPIDir - size of the buffer 
void GetMAPISVCPath(LPSTR szMAPIDir, ULONG cchMAPIDir) 
{ 
    HRESULT hRes = S_OK; 
    UINT uiRet = 0; 
    LONG lRet = 0; 
    BOOL bRet = true; 
    
    szMAPIDir[0] = &apos;\0&apos;; // Terminate string at position 0, safer if fail below 
    
    CHAR szSystemDir[MAX_PATH+1] = {0}; 
    
    // Get the system directory path 
    // (mapistub.dll and mapi32.dll reside here) 
    uiRet = GetSystemDirectoryA(szSystemDir, MAX_PATH); 
    if (uiRet &gt; 0) 
    { 
        CHAR szDLLPath[MAX_PATH+1] = {0}; 
       
        hRes = StringCchPrintfA(szDLLPath, MAX_PATH+1, &quot;%s\\%s&quot;,  
            szSystemDir, &quot;mapistub.dll&quot;); 
        if (SUCCEEDED(hRes)) 
        { 
            LPFGETCOMPONENTPATH pfnFGetComponentPath = NULL; 
          
            HMODULE hmodStub = 0; 
            HMODULE hmodMapi32 = 0; 
          
            // Load mapistub.dll 
            hmodStub = LoadLibraryA(szDLLPath); 
            if (hmodStub) 
            {    
                // Get the address of FGetComponentPath from the mapistub 
                pfnFGetComponentPath = (LPFGETCOMPONENTPATH)GetProcAddress( 
                    hmodStub, &quot;FGetComponentPath&quot;); 
            } 
          
            // If failed to get the address of FGetComponentPath, 
            // try mapi32.dll 
            if (!pfnFGetComponentPath) 
            { 
                hRes = StringCchPrintfA(szDLLPath, MAX_PATH+1, &quot;%s\\%s&quot;, 
                    szSystemDir, &quot;mapi32.dll&quot;); 
                if (SUCCEEDED(hRes)) 
                { 
                    // Load mapi32.dll 
                    hmodMapi32 = LoadLibraryA(szDLLPath); 
                    if (hmodMapi32) 
                    { 
                        // Get the address of FGetComponentPath from mapi32 
                        pfnFGetComponentPath = (LPFGETCOMPONENTPATH)GetProcAddress( 
                            hmodMapi32, &quot;FGetComponentPath&quot;); 
                    } 
                 } 
            } 
            if (pfnFGetComponentPath) 
            { 
                LPSTR szAppLCID = NULL; 
                LPSTR szOfficeLCID = NULL; 
                HKEY hMicrosoftOutlook = NULL; 
             
                lRet = RegOpenKeyEx( 
                    HKEY_LOCAL_MACHINE, 
                    _T(&quot;Software\\Clients\\Mail\\Microsoft Outlook&quot;), 
                    NULL, 
                    KEY_READ, 
                    &amp;hMicrosoftOutlook); 
             
                if (ERROR_SUCCESS == lRet &amp;&amp; hMicrosoftOutlook) 
                { 
                    HrGetRegMultiSZValueA(hMicrosoftOutlook, &quot;MSIApplicationLCID&quot;, (LPVOID*) &amp;szAppLCID); 
                    HrGetRegMultiSZValueA(hMicrosoftOutlook, &quot;MSIOfficeLCID&quot;, (LPVOID*) &amp;szOfficeLCID); 
                } 
             
                // Only passing a fixed value as the component ID for MAPI in this example 
                // In practice, must read from the registry the value of MSIComponentID 
                if (szAppLCID) 
                { 
                    bRet = pfnFGetComponentPath( 
                        &quot;{FF1D0740-D227-11D1-A4B0-006008AF820E}&quot;, szAppLCID, szMAPIDir, cchMAPIDir, true); 
                } 
                if ((!bRet || szMAPIDir[0] == _T(&apos;\0&apos;)) &amp;&amp; szOfficeLCID) 
                { 
                    bRet = pfnFGetComponentPath( 
                    &quot;{FF1D0740-D227-11D1-A4B0-006008AF820E}&quot;, szOfficeLCID, szMAPIDir, cchMAPIDir, true); 
                } 
                if (!bRet || szMAPIDir[0] == _T(&apos;\0&apos;)) 
                { 
                    bRet = pfnFGetComponentPath( 
                        &quot;{FF1D0740-D227-11D1-A4B0-006008AF820E}&quot;, NULL, szMAPIDir, cchMAPIDir, true); 
                } 
             
                // Got the path to msmapi32.dll - need to strip it 
                if (bRet &amp;&amp; szMAPIDir[0] != _T(&apos;\0&apos;)) 
                { 
                    LPSTR lpszSlash = NULL; 
                    LPSTR lpszCur = szMAPIDir; 
                
                    for (lpszSlash = lpszCur; *lpszCur; lpszCur = lpszCur++) 
                    { 
                        if (*lpszCur == _T(&apos;\\&apos;)) lpszSlash = lpszCur; 
                    } 
                   *lpszSlash = _T(&apos;\0&apos;); 
                } 
 
                delete[] szOfficeLCID; 
                delete[] szAppLCID; 
                if (hMicrosoftOutlook) RegCloseKey(hMicrosoftOutlook);       
            } 
             
            // If FGetComponentPath returns FALSE or if 
            // it returned nothing, or if failed to find an 
            // address of FGetComponentPath, then 
            // just default to the system directory 
            if (!bRet || szMAPIDir[0] == &apos;\0&apos;) 
            { 
                hRes = StringCchPrintfA( 
                    szMAPIDir, cchMAPIDir,&quot;%s&quot;, szSystemDir); 
            } 
          
            if (szMAPIDir[0] != _T(&apos;\0&apos;)) 
            { 
                hRes = StringCchPrintfA( 
                    szMAPIDir, cchMAPIDir, &quot;%s\\%s&quot;, szMAPIDir, &quot;MAPISVC.INF&quot;); 
            } 
          
            if (hmodMapi32) FreeLibrary(hmodMapi32); 
            if (hmodStub) FreeLibrary(hmodStub); 
        } 
    }    
}

```


