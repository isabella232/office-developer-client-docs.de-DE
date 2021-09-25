---
title: Initialisieren eines Anbieters von umschlossenem PST-Speicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 07633717-ba4c-b146-ad65-60b37ab98ab6
description: 'Last modified: October 05, 2012'
ms.openlocfilehash: 3601e359eef6d798170d10e2debcb3613245f30c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571654"
---
# <a name="initializing-a-wrapped-pst-store-provider"></a>Initialisieren eines Anbieters von umschlossenem PST-Speicher

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zum Implementieren eines Anbieters von PST-Speicher (Wrapped Personal Folders File) müssen Sie den Anbieter des umschlossenen PST-Speichers initialisieren, indem Sie die **[MSProviderInit-Funktion](msproviderinit.md)** als Einstiegspunkt verwenden. Nachdem die DLL des Anbieters initialisiert wurde, konfiguriert die **[MSGSERVICEENTRY-Funktion](msgserviceentry.md)** den umschlossenen PST-Speicheranbieter. 
  
In diesem Thema werden die **MSProviderInit-Funktion** und die **MSGSERVICEENTRY-Funktion** anhand von Codebeispielen aus dem Sample Wrapped PST Store Provider veranschaulicht. Das Beispiel implementiert einen umschlossenen PST-Anbieter, der in Verbindung mit der Replikations-API verwendet werden soll. Weitere Informationen zum Herunterladen und Installieren des Beispiel-Anbieters für umbrochene PST-Store finden Sie unter [Installieren des Beispiel-Anbieters für umschlossene PST-Store.](installing-the-sample-wrapped-pst-store-provider.md) Weitere Informationen zur Replikations-API finden Sie unter ["Informationen zur Replikations-API".](about-the-replication-api.md)
  
Nachdem Sie einen anbieterumschlossenen PST-Speicher initialisiert haben, müssen Sie Funktionen implementieren, damit sich MAPI und der MAPI-Spooler beim Nachrichtenspeicheranbieter anmelden können. Weitere Informationen finden Sie unter ["Anmelden bei einem umschlossenen PST-Store Anbieter".](logging-on-to-a-wrapped-pst-store-provider.md)
  
## <a name="initialization-routine"></a>Initialisierungsroutine

Alle anbieterumschlossenen PST-Speicher müssen die **[MSProviderInit-Funktion](msproviderinit.md)** als Einstiegspunkt implementieren, um die DLL des Anbieters zu initialisieren. **MSProviderInit** überprüft, ob die Versionsnummer der `ulMAPIVer` Dienstanbieterschnittstelle, mit der aktuellen Versionsnummer kompatibel ist. `CURRENT_SPI_VERSION` Die Funktion speichert die MAPI-Speicherverwaltungsroutinen in den  `g_lpAllocateBuffer`  `g_lpAllocateMore` , und  `g_lpFreeBuffer` Parametern. Diese Speicherverwaltungsroutinen sollten in der gesamten Implementierung des umschlossenen PST-Speichers für die Speicherzuweisung und -zuordnung verwendet werden. 
  
### <a name="msproviderinit-example"></a>MSProviderInit() (Beispiel)

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

### <a name="wrapped-pst-and-unicode-paths"></a>Umschlossene PST- und Unicode-Pfade

Um das ursprüngliche in Microsoft Visual Studio 2008 vorbereitete Beispiel so umzurüsten, dass Unicode-Pfade für die Verwendung in Unicode-fähigen Microsoft Outlook 2010 und Outlook 2013 verwendet werden, sollte die **CreateStoreEntryID-Routine,** die den Eintragsbezeichner erzeugt, ein Format für ASCII-Pfade und ein weiteres für Unicode-Pfade verwenden. Diese werden im folgenden Beispiel als Strukturen dargestellt. 
  
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
> Die Unterschiede in diesen Strukturen sind zwei NULL-Bytes vor einem Unicode-Pfad. Wenn Sie den Eintragsbezeichner in der folgenden "Diensteintragsroutine" interpretieren müssen, können Sie anhand einer Möglichkeit ermitteln, ob dies der Fall ist oder nicht, zuerst als EIDMS umwandeln und dann überprüfen, ob szPath[0] NULL ist. Wenn ja, wandeln Sie es stattdessen in EIDMSW um. 
  
## <a name="service-entry-routine"></a>Diensteintragsroutine

Die **[MSGSERVICEENTRY-Funktion](msgserviceentry.md)** ist der Einstiegspunkt für den Nachrichtendienst, an dem der anbieterumschlossene PST-Speicher konfiguriert ist. Die Funktion ruft  `GetMemAllocRoutines()` auf, um die MAPI-Speicherverwaltungsroutinen abzurufen. Die Funktion verwendet den  `lpProviderAdmin` Parameter, um den Profilabschnitt für den Anbieter zu suchen, und legt die Eigenschaften im Profil fest. 
  
### <a name="serviceentry-example"></a>ServiceEntry() (Beispiel)

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

- [Informationen zum Beispiel für pst-Store-Anbieter mit Umschlossenen](about-the-sample-wrapped-pst-store-provider.md)
- [Installieren des Beispielanbieters für pst-Store](installing-the-sample-wrapped-pst-store-provider.md)
- [Anmelden bei einem Anbieter von umschlossenen PST-Store](logging-on-to-a-wrapped-pst-store-provider.md)
- [Verwenden eines Anbieters von umschlossenen PST-Store](using-a-wrapped-pst-store-provider.md)
- [Herunterfahren eines Anbieters von umschlossenen PST-Store](shutting-down-a-wrapped-pst-store-provider.md)

