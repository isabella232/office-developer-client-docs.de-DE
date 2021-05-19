---
title: Abrufen des Pfads einer bestimmten Version von MAPI für den Stanard-Mail-Client
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ee7fb05-cfb3-6b68-5a9a-1d6375f2e879
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1992e34a684a6b5894963eae0c299b21c064578c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346459"
---
# <a name="get-the-path-of-a-specific-version-of-mapi-for-the-default-mail-client"></a>Abrufen des Pfads einer bestimmten Version von MAPI für den Stanard-Mail-Client

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält ein Codebeispiel in C++, das zeigt, wie Sie den Pfad einer bestimmten Version von MAPI abrufen, die vom Standard-E-Mail-Client auf einem Computer verwendet wird. MAPI-E-Mail-Clients können in der Registrierung eine benutzerdefinierte DLL angeben, an die die MAPI-Stubbibliothek MAPI-Aufrufe laden und senden soll. Der Registrierungsschlüssel, der für diese benutzerdefinierte DLL für einen Standard-E-Mail-Client festgelegt werden soll, ist **MSIComponentID** unter **dem HKLM\Software\Clients\Mail-Schlüssel** des Standard-E-Mail-Clients. Die [FGetComponentPath-Funktion,](fgetcomponentpath.md) die von der MAPI-Stubbibliothek mapistub.dll exportiert wird, kann den Pfad zur benutzerdefinierten Version von MAPI zurückgeben, die durch den **Registrierungsschlüssel MSIComponentID** angegeben wird. 
  
Dieses Codebeispiel enthält zwei Funktionen:  `HrGetRegMultiSZValueA` und  `GetMAPISVCPath` . Die  `GetMAPISVCPath` Funktion verwendet [FGetComponentPath,](fgetcomponentpath.md) um den Pfad zur benutzerdefinierten Version von MAPI zu erhalten. Es wird davon ausgegangen, dass der Standard-E-Mail-Client Microsoft Office Outlook 2007 ist und **an FGetComponentPath** den Wert übergibt, den Outlook 2007 als Komponenten-ID von MAPI für den  `{FF1D0740-D227-11D1-A4B0-006008AF820E}` **MSIComponentID-Registrierungsschlüssel** legt. 
  
> [!NOTE]
> In der Praxis sollten Sie nicht davon ausgehen, dass der Wert , immer die Komponenten-ID von MAPI ist, und ihn direkt an `{FF1D0740-D227-11D1-A4B0-006008AF820E}` **FGetComponentPath übergeben.** Um zuverlässig herauszufinden, welche Version von MAPI Outlook auf einem Computer verwendet, müssen Sie aus der Registrierung den Wert von **MSIComponentID** lesen und an **FGetComponentPath übergeben.** 
  
In den folgenden Schritten wird  `GetMAPISVCPath` beschrieben, wie dies funktioniert. 
  
1. Lädt die MAPI-Stubbibliothek mapistub.dll aus dem Systemverzeichnis.
    
2. Angenommen, mapistub.dll die **FGetComponentPath-Funktion** exportiert, wird versucht, die Adresse dieser Funktion aus mapistub.dll. 
    
3. Wenn beim Abrufen der Adresse aus mapistub.dll fehlert, wird versucht, die Adresse aus dem mapi32.dll.
    
4. Wenn das Abrufen der Adresse von **FGetComponentPath** erfolgreich ist, wird die Registrierung geöffnet und die Funktion verwendet, um die Registrierungswerte unter  `HrGetRegMultiSZValueA` **HKLM\Software\Clients\Mail\Microsoft Outlook** zu lesen. 
    
5. Ruft **FGetComponentPath auf,** um den Von Outlook 2007 verwendeten Pfad zur  `{FF1D0740-D227-11D1-A4B0-006008AF820E}` MapI-Version zu erhalten.
    
Beachten Sie, dass zum Unterstützen lokalisierter Kopien von MAPI für englische und nicht englische Locales im Codebeispiel die Werte für die Unterschlüssel **MSIApplicationLCID** und **MSIOfficeLCID** gelesen und **FGetComponentPath aufruft,** zunächst **MSIApplicationLCID** als  *szQualifier*  angegeben und dann **erneut MSIOfficeLCID** als  *szQualifier*  angegeben wird. Weitere Informationen zu Registrierungsschlüsseln für E-Mail-Clients, die nicht englische Sprachen unterstützen, finden Sie unter [Einrichten der MSI-Schlüssel für Ihre MAPI-DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).
  
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


