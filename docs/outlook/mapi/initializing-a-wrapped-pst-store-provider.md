---
title: Initialisieren von einem gepackten PST-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07633717-ba4c-b146-ad65-60b37ab98ab6
description: 'Zuletzt geändert: 05 Oktober 2012'
ms.openlocfilehash: a332c63814163579d5fe8ab365145e9583fa6c97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792703"
---
# <a name="initializing-a-wrapped-pst-store-provider"></a>Initialisieren von einem gepackten PST-Anbieter

**Betrifft**: Outlook 
  
Um einen gepackten Anbieter für Persönliche Ordner-Datei (PST) anmelden zu implementieren, müssen Sie den gepackten PST-Speicheranbieter mithilfe der **[MSProviderInit](msproviderinit.md)** -Funktion als Einstiegspunkt initialisieren. Nachdem die DLL des Anbieters initialisiert wurde, konfiguriert die **[MSGSERVICEENTRY](msgserviceentry.md)** -Funktion den gepackten PST-Anbieter. 
  
In diesem Thema werden die **MSProviderInit** und der **MSGSERVICEENTRY** -Funktion mithilfe von Codebeispielen aus der umbrochen PST Store Beispielanbieter veranschaulicht. Das Beispiel implementiert einen gepackten PST-Anbieter, der in Verbindung mit der API für die Replikation verwendet werden soll. Weitere Informationen zum Herunterladen und Installieren der umbrochen PST Store Beispielanbieter finden Sie unter [Sample umfließendem PST Store Provider installieren](installing-the-sample-wrapped-pst-store-provider.md). Weitere Informationen zur Replikation-API finden Sie unter [Über die Replikation-API](about-the-replication-api.md).
  
Nachdem Sie einen gepackten PST-Anbieter initialisiert haben, müssen Sie Funktionen implementieren, sodass MAPI- und die MAPI-Warteschlange auf den Anbieter für die Nachricht anmelden anmelden können. Weitere Informationen finden Sie unter [Protokollierung für den Zugriff auf einen Anbieter umfließendem PST anmelden](logging-on-to-a-wrapped-pst-store-provider.md).
  
## <a name="initialization-routine"></a>Initialisierungsroutine

Alle gepackten PST-Speicher-Anbieter müssen die **[MSProviderInit](msproviderinit.md)** -Funktion als Einstiegspunkt für die DLL des Anbieters initialisieren implementieren. **MSProviderInit** überprüft, ob die Versionsnummer der Anbieterschnittstelle Service `ulMAPIVer`, ist kompatibel mit die aktuelle Versionsnummer `CURRENT_SPI_VERSION`. Die Funktion speichert den MAPI-Speicher Management Routinen in die `g_lpAllocateBuffer`, `g_lpAllocateMore`, und `g_lpFreeBuffer` Parameter. Diese Speicher Management Routinen sollte während der gesamten Implementierung gepackten PST-Speicher für die Zuweisung von Arbeitsspeicher und Freigabe verwendet werden. 
  
### <a name="msproviderinit-example"></a>MSProviderInit()-Beispiel

```cpp
STDINITMETHODIMP MSProviderInit ( 
    HINSTANCE /*hInstance*/, 
    LPMALLOC lpMalloc, 
    LPALLOCATEBUFFER lpAllocateBuffer, 
    LPALLOCATEMORE lpAllocateMore, 
    LPFREEBUFFER lpFreeBuffer, 
    ULONG ulFlags, 
    ULONG ulMAPIVer, 
    ULONG FAR * lpulProviderVer, 
    LPMSPROVIDER FAR * lppMSProvider) 
{ 
    Log(true,"MSProviderInit function called\n"); 
    if (!lppMSProvider || !lpulProviderVer) return MAPI_E_INVALID_PARAMETER; 
    HRESULT hRes = S_OK; 
 
    *lppMSProvider = NULL; 
    *lpulProviderVer = CURRENT_SPI_VERSION; 
    if (ulMAPIVer < CURRENT_SPI_VERSION) 
    { 
        Log(true,"MSProviderInit: The version of the subsystem cannot handle this" 
            + "version of the provider\n"); 
        return MAPI_E_VERSION; 
    } 
 
    Log(true,"MSProviderInit: saving off memory management routines\n"); 
    g_lpAllocateBuffer = lpAllocateBuffer; 
    g_lpAllocateMore = lpAllocateMore; 
    g_lpFreeBuffer = lpFreeBuffer; 
    HMODULE hm = LoadLibrary("C:\\Program Files\\Common Files\\System" + 
        "\\MSMAPI\\1033\\MSPST32.dll" ); 
    if (!hm) hm = LoadLibrary("C:\\Program Files\\Microsoft Office\\Office12" + 
        "\\MSPST32.dll" ); 
    Log(true,"LoadLibrary returned 0x%08X\n", hm); 
 
    LPMSPROVIDERINIT pMsProviderInit = NULL; 
    if (hm) 
    { 
        pMsProviderInit = (LPMSPROVIDERINIT)GetProcAddress(hm, "MSProviderInit"); 
        Log(true,"GetProcAddress returned 0x%08X\n", pMsProviderInit); 
    } 
    else hRes = E_OUTOFMEMORY; 
    if (pMsProviderInit) 
    { 
        Log(true,"Calling pMsProviderInit\n"); 
        CMSProvider* pWrappedProvider = NULL; 
        LPMSPROVIDER pSyncProviderObj = NULL; 
        hRes = pMsProviderInit( 
            hm,// not hInstance: first param is handle of module in which the function lives 
            lpMalloc, 
            lpAllocateBuffer, 
            lpAllocateMore, 
            lpFreeBuffer, 
            ulFlags, 
            ulMAPIVer, 
            lpulProviderVer, 
            &pSyncProviderObj                         
            ); 
        Log(true,"pMsProviderInit returned 0x%08X\n", hRes); 
        if (SUCCEEDED(hRes)) 
        { 
            pWrappedProvider = new CMSProvider (pSyncProviderObj); 
            if (NULL == pWrappedProvider) 
            { 
                Log(true,"MSProviderInit: Failed to allocate new CMSProvider object\n"); 
                hRes = E_OUTOFMEMORY; 
            } 
            // Copy pointer to the allocated object back into the  
            //return IMSProvider object pointer 
            *lppMSProvider = pWrappedProvider; 
        } 
    } 
    else hRes = E_OUTOFMEMORY; 
    return hRes; 
}
```

### <a name="wrapped-pst-and-unicode-paths"></a>Gepackten PST- und Unicode-Pfade

Um das ursprüngliche Beispiel in Microsoft Visual Studio 2008 Verwendung von Unicode-Pfade zum NST für die Verwendung in Unicode-aktivierten Microsoft Outlook 2010 und Outlook 2013 vorbereitete überarbeiten, sollten die **CreateStoreEntryID** -Routine, die die Eintrags-ID erstellt, das verwenden. ein Format für die ASCII-Pfade und ein weiteres für Unicode-Pfade. Diese werden als Strukturen im folgenden Beispiel dargestellt. 
  
```cpp
typedef struct                              // short format
{
         BYTE             rgbFlags[4];     // MAPI-defined flags
         MAPIUID          uid;             // PST provider MUID
         BYTE             bReserved;       // Reserved (must be zero)
         CHAR             szPath[1];       // Full path to store (ASCII)
 } EIDMS;
// Unicode version of EIDMSW is an extension of EIDMS
// and szPath is always NULL
typedef struct                              // Long format to support Unicode path and name
{
         BYTE             rgbFlags[4];     // MAPI-defined flags
         MAPIUID          uid;             // PST provider MUID
         BYTE             bReserved;       // Reserved (must be zero)
         CHAR             szPath[1];       // ASCII path to store is always NULL
         WCHAR            wzPath[1];       // Full path to store (Unicode)
} EIDMSW;
```

> [!IMPORTANT]
> Die Unterschiede zwischen diesen Strukturen sind zwei NULL-Bytes vor einem Unicode-Pfad. Wenn Sie interpretiert die Eintrags-ID in der "Service Eintrag routinemäßige", der die befolgt werden müssen, wäre eine Möglichkeit zum bestimmen, ob dies der Fall ist, wandeln Sie wie EIDMS zuerst, überprüfen Sie, ob die SzPath [0] NULL ist. Es ist, stattdessen als EIDMSW umgewandelt. 
  
## <a name="service-entry-routine"></a>Diensteintrag routine

Die **[MSGSERVICEENTRY](msgserviceentry.md)** -Funktion ist der Einstiegspunkt des Nachricht, in der gepackten PST Informationsdienst konfiguriert ist. Die Funktionsaufrufe `GetMemAllocRoutines()` an den MAPI-Speicher Management Routinen abzurufen. Die Funktion verwendet die `lpProviderAdmin` Parameter Abschnitts Profile für den Anbieter und legt die Eigenschaften im Benutzerprofil zu finden. 
  
### <a name="serviceentry-example"></a>ServiceEntry()-Beispiel

```cpp
HRESULT STDAPICALLTYPE ServiceEntry ( 
    HINSTANCE /*hInstance*/, 
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR *lppMapiError) 
{ 
    if (!lpMAPISup || !lpProviderAdmin) return MAPI_E_INVALID_PARAMETER; 
    HRESULT         hRes = S_OK; 
    Log(true,"ServiceEntry function called\n"); 
    Log(true,"About to call NSTServiceEntry\n"); 
 
    if (MSG_SERVICE_INSTALL         == ulContext || 
        MSG_SERVICE_DELETE            == ulContext || 
        MSG_SERVICE_UNINSTALL        == ulContext || 
        MSG_SERVICE_PROVIDER_CREATE == ulContext || 
        MSG_SERVICE_PROVIDER_DELETE == ulContext) 
    { 
        // These contexts are not supported 
        return MAPI_E_NO_SUPPORT; 
    } 
 
    // Get memory routines 
    hRes = lpMAPISup-> 
        GetMemAllocRoutines(&g_lpAllocateBuffer,&g_lpAllocateMore,&g_lpFreeBuffer); 
    HMODULE hm = LoadLibrary("C:\\Program Files\\Common Files\\System" + 
        "\\MSMAPI\\1033\\MSPST32.dll" ); 
    if (!hm) hm = LoadLibrary("C:\\Program Files\\Microsoft Office\\Office12" + 
        "\\MSPST32.dll" ); 
    Log(true, "Got module 0x%08X\n", hm); 
    if (!hm) return E_OUTOFMEMORY; 
    LPMSGSERVICEENTRY pNSTServiceEntry =  
        (LPMSGSERVICEENTRY)GetProcAddress(hm, "NSTServiceEntry"); 
    Log(true, "Got procaddress  0x%08X\n", pNSTServiceEntry); 
    if (!pNSTServiceEntry) return E_OUTOFMEMORY; 
 
    // Get profile section 
    LPPROFSECT lpProfSect = NULL; 
    hRes = lpProviderAdmin-> 
        OpenProfileSection((LPMAPIUID) NULL, NULL, MAPI_MODIFY, &lpProfSect); 
    // Set passed in props into the profile 
    if (lpProps && cValues) 
    { 
        hRes = lpProfSect->SetProps(cValues,lpProps,NULL); 
    } 
    // Make sure there is a store path set 
    if (SUCCEEDED(hRes)) hRes = SetOfflineStoreProps(lpProfSect,ulUIParam); 
    ULONG            ulProfProps = 0; 
    LPSPropValue    lpProfProps = NULL; 
 
    // Evaluate props 
    hRes = lpProfSect->GetProps((LPSPropTagArray)&sptClientProps, 
                                fMapiUnicode, 
                                &ulProfProps, 
                                &lpProfProps); 
    if (SUCCEEDED(hRes)) 
    { 
        CSupport * pMySup = NULL; 
        pMySup = new CSupport(lpMAPISup, lpProfSect); 
        if (!pMySup) 
        { 
            Log(true,"MSProviderInit: Failed to allocate new CSupport object\n"); 
            hRes = E_OUTOFMEMORY; 
        } 
        if (SUCCEEDED(hRes)) 
        { 
            hRes = pNSTServiceEntry( 
                hm,  
                lpMalloc, 
                pMySup, 
                ulUIParam, 
                ulFlags, 
                ulContext, 
                ulProfProps, 
                lpProfProps, 
                NULL,//pAdminProvObj, //Don't pass this when creating an NST 
                lppMapiError); 
            if (SUCCEEDED(hRes)) 
            { 
                // Finish setting up the profile 
                hRes = InitStoreProps( 
                    lpMAPISup,  
                    lpProfSect,  
                    lpProviderAdmin); 
                hRes = lpProfSect->SaveChanges(KEEP_OPEN_READWRITE); 
            } 
        } 
    } 
    Log(true, "Ran pNSTServiceEntry 0x%08X\n", hRes); 
    MyFreeBuffer(lpProfProps); 
    if (lpProfSect) lpProfSect->Release(); 
 
    return hRes; 
}
```

## <a name="see-also"></a>Siehe auch

- [Zum Beispiel umgebrochen PST-Anbieter](about-the-sample-wrapped-pst-store-provider.md)
- [Installieren des Beispiels umfließendem PST-Anbieter](installing-the-sample-wrapped-pst-store-provider.md)
- [Anmelden bei einem Anbieter gepackten PST-Datei](logging-on-to-a-wrapped-pst-store-provider.md)
- [Verwenden eines Anbieters gepackten PST-Speichers](using-a-wrapped-pst-store-provider.md)
- [Herunterfahren von einem Anbieter gepackten PST-Datei](shutting-down-a-wrapped-pst-store-provider.md)

