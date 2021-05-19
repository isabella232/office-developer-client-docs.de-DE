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
# <a name="get-the-path-of-a-specific-version-of-mapi-for-the-default-mail-client"></a><span data-ttu-id="af870-103">Abrufen des Pfads einer bestimmten Version von MAPI für den Stanard-Mail-Client</span><span class="sxs-lookup"><span data-stu-id="af870-103">Get the path of a specific version of MAPI for the default mail client</span></span>

<span data-ttu-id="af870-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af870-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af870-105">Dieses Thema enthält ein Codebeispiel in C++, das zeigt, wie Sie den Pfad einer bestimmten Version von MAPI abrufen, die vom Standard-E-Mail-Client auf einem Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="af870-105">This topic includes a code sample in C++ that shows how to obtain the path of a specific version of MAPI that is used by the default mail client on a computer.</span></span> <span data-ttu-id="af870-106">MAPI-E-Mail-Clients können in der Registrierung eine benutzerdefinierte DLL angeben, an die die MAPI-Stubbibliothek MAPI-Aufrufe laden und senden soll.</span><span class="sxs-lookup"><span data-stu-id="af870-106">MAPI mail clients have an option to specify in the registry a custom DLL that the MAPI stub library should load and dispatch MAPI calls to.</span></span> <span data-ttu-id="af870-107">Der Registrierungsschlüssel, der für diese benutzerdefinierte DLL für einen Standard-E-Mail-Client festgelegt werden soll, ist **MSIComponentID** unter **dem HKLM\Software\Clients\Mail-Schlüssel** des Standard-E-Mail-Clients.</span><span class="sxs-lookup"><span data-stu-id="af870-107">The registry key to set for this custom DLL for a default mail client is **MSIComponentID**, under the **HKLM\Software\Clients\Mail** key of the default mail client.</span></span> <span data-ttu-id="af870-108">Die [FGetComponentPath-Funktion,](fgetcomponentpath.md) die von der MAPI-Stubbibliothek mapistub.dll exportiert wird, kann den Pfad zur benutzerdefinierten Version von MAPI zurückgeben, die durch den **Registrierungsschlüssel MSIComponentID** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="af870-108">The [FGetComponentPath](fgetcomponentpath.md) function, exported by the MAPI stub library, mapistub.dll, can return the path to the custom version of MAPI specified by the **MSIComponentID** registry key.</span></span> 
  
<span data-ttu-id="af870-109">Dieses Codebeispiel enthält zwei Funktionen:  `HrGetRegMultiSZValueA` und  `GetMAPISVCPath` .</span><span class="sxs-lookup"><span data-stu-id="af870-109">This code sample includes two functions:  `HrGetRegMultiSZValueA` and  `GetMAPISVCPath`.</span></span> <span data-ttu-id="af870-110">Die  `GetMAPISVCPath` Funktion verwendet [FGetComponentPath,](fgetcomponentpath.md) um den Pfad zur benutzerdefinierten Version von MAPI zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="af870-110">The  `GetMAPISVCPath` function uses [FGetComponentPath](fgetcomponentpath.md) to obtain the path to the custom version of MAPI.</span></span> <span data-ttu-id="af870-111">Es wird davon ausgegangen, dass der Standard-E-Mail-Client Microsoft Office Outlook 2007 ist und **an FGetComponentPath** den Wert übergibt, den Outlook 2007 als Komponenten-ID von MAPI für den  `{FF1D0740-D227-11D1-A4B0-006008AF820E}` **MSIComponentID-Registrierungsschlüssel** legt.</span><span class="sxs-lookup"><span data-stu-id="af870-111">It assumes that the default mail client is Microsoft Office Outlook 2007, and passes to **FGetComponentPath** the value,  `{FF1D0740-D227-11D1-A4B0-006008AF820E}`, that Outlook 2007 sets as the component ID of MAPI for the **MSIComponentID** registry key.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="af870-112">In der Praxis sollten Sie nicht davon ausgehen, dass der Wert , immer die Komponenten-ID von MAPI ist, und ihn direkt an `{FF1D0740-D227-11D1-A4B0-006008AF820E}` **FGetComponentPath übergeben.**</span><span class="sxs-lookup"><span data-stu-id="af870-112">In practice, you should not assume the value,  `{FF1D0740-D227-11D1-A4B0-006008AF820E}`, is always the component ID of MAPI and directly pass it to **FGetComponentPath**.</span></span> <span data-ttu-id="af870-113">Um zuverlässig herauszufinden, welche Version von MAPI Outlook auf einem Computer verwendet, müssen Sie aus der Registrierung den Wert von **MSIComponentID** lesen und an **FGetComponentPath übergeben.**</span><span class="sxs-lookup"><span data-stu-id="af870-113">To reliably find out which version of MAPI Outlook uses on a computer, you must read from the registry the value of **MSIComponentID** and pass it to **FGetComponentPath**.</span></span> 
  
<span data-ttu-id="af870-114">In den folgenden Schritten wird  `GetMAPISVCPath` beschrieben, wie dies funktioniert.</span><span class="sxs-lookup"><span data-stu-id="af870-114">The following steps describe how  `GetMAPISVCPath` does this.</span></span> 
  
1. <span data-ttu-id="af870-115">Lädt die MAPI-Stubbibliothek mapistub.dll aus dem Systemverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="af870-115">Loads the MAPI stub library, mapistub.dll, from the system directory.</span></span>
    
2. <span data-ttu-id="af870-116">Angenommen, mapistub.dll die **FGetComponentPath-Funktion** exportiert, wird versucht, die Adresse dieser Funktion aus mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="af870-116">Assumes that mapistub.dll exports the **FGetComponentPath** function, it tries to get the address of this function from mapistub.dll.</span></span> 
    
3. <span data-ttu-id="af870-117">Wenn beim Abrufen der Adresse aus mapistub.dll fehlert, wird versucht, die Adresse aus dem mapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="af870-117">If getting the address from mapistub.dll fails, it tries to get the address from mapi32.dll.</span></span>
    
4. <span data-ttu-id="af870-118">Wenn das Abrufen der Adresse von **FGetComponentPath** erfolgreich ist, wird die Registrierung geöffnet und die Funktion verwendet, um die Registrierungswerte unter  `HrGetRegMultiSZValueA` **HKLM\Software\Clients\Mail\Microsoft Outlook** zu lesen.</span><span class="sxs-lookup"><span data-stu-id="af870-118">If getting the address of **FGetComponentPath** succeeds, it opens the registry and uses the  `HrGetRegMultiSZValueA` function to read the registry values under **HKLM\Software\Clients\Mail\Microsoft Outlook**.</span></span> 
    
5. <span data-ttu-id="af870-119">Ruft **FGetComponentPath auf,** um den Von Outlook 2007 verwendeten Pfad zur  `{FF1D0740-D227-11D1-A4B0-006008AF820E}` MapI-Version zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="af870-119">Calls **FGetComponentPath**, specifying the value,  `{FF1D0740-D227-11D1-A4B0-006008AF820E}`, to obtain the path to the version of MAPI that Outlook 2007 uses.</span></span>
    
<span data-ttu-id="af870-120">Beachten Sie, dass zum Unterstützen lokalisierter Kopien von MAPI für englische und nicht englische Locales im Codebeispiel die Werte für die Unterschlüssel **MSIApplicationLCID** und **MSIOfficeLCID** gelesen und **FGetComponentPath aufruft,** zunächst **MSIApplicationLCID** als  *szQualifier*  angegeben und dann **erneut MSIOfficeLCID** als  *szQualifier*  angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="af870-120">Note that to support localized copies of MAPI for English and non-English locales, the code sample reads the values for the **MSIApplicationLCID** and **MSIOfficeLCID** subkeys and calls **FGetComponentPath**, first specifying **MSIApplicationLCID** as  *szQualifier*  , and then again specifying **MSIOfficeLCID** as  *szQualifier*  .</span></span> <span data-ttu-id="af870-121">Weitere Informationen zu Registrierungsschlüsseln für E-Mail-Clients, die nicht englische Sprachen unterstützen, finden Sie unter [Einrichten der MSI-Schlüssel für Ihre MAPI-DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="af870-121">For more information about registry keys for mail clients that support non-English languages, see [Setting Up the MSI Keys for Your MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span></span>
  
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


