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
  
Dieses Thema enthält ein Codebeispiel in C++, das zeigt, wie der Pfad einer bestimmten Version von MAPI abgerufen wird, die vom Standard-e-Mail-Client auf einem Computer verwendet wird. MAPI-e-Mail-Clients können in der Registrierung eine benutzerdefinierte DLL angeben, die von der MAPI-Stub-Bibliothek geladen und MAPI-Aufrufe an gesendet werden soll. Der Registrierungsschlüssel, der für diese benutzerdefinierte DLL für einen standardmäßigen e-Mail-Client festgelegt werden soll, lautet **MSIComponentID**unter dem **HKLM\Software\Clients\Mail** -Schlüssel des Standard-e-Mail-Clients. Die [FGetComponentPath](fgetcomponentpath.md) -Funktion, die von der MAPI-Stub-Bibliothek, mapistub. dll, exportiert wird, kann den Pfad zur BENUTZERdefinierten MAPI-Version zurückgeben, die durch den **MSIComponentID** -Registrierungsschlüssel angegeben wird. 
  
Dieses Codebeispiel umfasst zwei Funktionen: `HrGetRegMultiSZValueA` und `GetMAPISVCPath`. Die `GetMAPISVCPath` Funktion verwendet [FGetComponentPath](fgetcomponentpath.md) , um den Pfad zur benutzerdefinierten Version von MAPI abzurufen. Es wird davon ausgegangen, dass der standardmäßige e-Mail- **** Client Microsoft Office Outlook `{FF1D0740-D227-11D1-A4B0-006008AF820E}`2007 ist und an FGetComponentPath den Wert übergibt, der von Outlook 2007 als Komponenten-ID von MAPI für den **MSIComponentID** -Registrierungsschlüssel festgelegt wird. 
  
> [!NOTE]
> In der Praxis sollten Sie nicht davon ausgehen, `{FF1D0740-D227-11D1-A4B0-006008AF820E}`dass der Wert, ist immer die Komponenten-ID von MAPI und direkt an **FGetComponentPath**. Um zuverlässig herauszufinden, welche Version von MAPI Outlook auf einem Computer verwendet wird, müssen Sie den Wert von **MSIComponentID** aus der Registrierung lesen und an **FGetComponentPath**weiterleiten. 
  
In den folgenden Schritten wird `GetMAPISVCPath` beschrieben, wie dies funktioniert. 
  
1. Lädt die MAPI-Stub-Bibliothek mapistub. dll aus dem Systemverzeichnis.
    
2. Wird davon ausgeGangen, dass mapistub. dll die **FGetComponentPath** -Funktion exportiert, versucht Sie, die Adresse dieser Funktion aus mapistub. dll abzurufen. 
    
3. Wenn die Adresse von mapistub. dll nicht abgerufen wird, versucht Sie, die Adresse aus Mapi32. dll abzurufen.
    
4. Wenn die Adresse von **FGetComponentPath** erfolgreich abgerufen wird, wird die Registrierung geöffnet, und die `HrGetRegMultiSZValueA` -Funktion wird verwendet, um die Registrierungswerte unter **HKLM\Software\Clients\Mail\Microsoft Outlook**zu lesen. 
    
5. Ruft **FGetComponentPath** `{FF1D0740-D227-11D1-A4B0-006008AF820E}`auf, um den Pfad zur Version von MAPI abzurufen, die von Outlook 2007 verwendet wird.
    
Beachten Sie, dass zur Unterstützung lokalisierter Kopien von MAPI für englische und nicht-englische Gebietsschemata das Codebeispiel die Werte für die **MSIApplicationLCID** und **MSIOfficeLCID** liest und **FGetComponentPath**aufruft, indem **Sie zuerst MSIApplicationLCID** als *szQualifier* und dann erneut angeben von **MSIOfficeLCID** als *szQualifier* . Weitere Informationen zu Registrierungsschlüsseln für e-Mail-Clients, die nicht-englische Sprachen unterstützen, finden Sie unter [Einrichten der MSI-Schlüssel für Ihre MAPI-DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).
  
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


