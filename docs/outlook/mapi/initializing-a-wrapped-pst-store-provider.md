---
title: Initialisieren von einem gepackten PST-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07633717-ba4c-b146-ad65-60b37ab98ab6
description: 'Zuletzt geändert: 05 Oktober 2012'
ms.openlocfilehash: c39f66917ecc080785b3a3e91506d3994427ca62
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569078"
---
# <a name="initializing-a-wrapped-pst-store-provider"></a><span data-ttu-id="8f483-103">Initialisieren von einem gepackten PST-Anbieter</span><span class="sxs-lookup"><span data-stu-id="8f483-103">Initializing a wrapped PST store provider</span></span>

<span data-ttu-id="8f483-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f483-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f483-105">Um einen gepackten Anbieter für Persönliche Ordner-Datei (PST) anmelden zu implementieren, müssen Sie den gepackten PST-Speicheranbieter mithilfe der **[MSProviderInit](msproviderinit.md)** -Funktion als Einstiegspunkt initialisieren.</span><span class="sxs-lookup"><span data-stu-id="8f483-105">To implement a wrapped Personal Folders file (PST) store provider, you must initialize the wrapped PST store provider by using the **[MSProviderInit](msproviderinit.md)** function as an entry point.</span></span> <span data-ttu-id="8f483-106">Nachdem die DLL des Anbieters initialisiert wurde, konfiguriert die **[MSGSERVICEENTRY](msgserviceentry.md)** -Funktion den gepackten PST-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="8f483-106">After the provider's DLL is initialized, the **[MSGSERVICEENTRY](msgserviceentry.md)** function configures the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="8f483-107">In diesem Thema werden die **MSProviderInit** und der **MSGSERVICEENTRY** -Funktion mithilfe von Codebeispielen aus der umbrochen PST Store Beispielanbieter veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="8f483-107">In this topic, the **MSProviderInit** function and the **MSGSERVICEENTRY** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="8f483-108">Das Beispiel implementiert einen gepackten PST-Anbieter, der in Verbindung mit der API für die Replikation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f483-108">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="8f483-109">Weitere Informationen zum Herunterladen und Installieren der umbrochen PST Store Beispielanbieter finden Sie unter [Sample umfließendem PST Store Provider installieren](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8f483-109">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="8f483-110">Weitere Informationen zur Replikation-API finden Sie unter [Über die Replikation-API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="8f483-110">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="8f483-111">Nachdem Sie einen gepackten PST-Anbieter initialisiert haben, müssen Sie Funktionen implementieren, sodass MAPI- und die MAPI-Warteschlange auf den Anbieter für die Nachricht anmelden anmelden können.</span><span class="sxs-lookup"><span data-stu-id="8f483-111">After you have initialized a wrapped PST store provider, you must implement functions so that MAPI and the MAPI spooler can log onto the message store provider.</span></span> <span data-ttu-id="8f483-112">Weitere Informationen finden Sie unter [Protokollierung für den Zugriff auf einen Anbieter umfließendem PST anmelden](logging-on-to-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8f483-112">For more information, see [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="initialization-routine"></a><span data-ttu-id="8f483-113">Initialisierungsroutine</span><span class="sxs-lookup"><span data-stu-id="8f483-113">Initialization routine</span></span>

<span data-ttu-id="8f483-114">Alle gepackten PST-Speicher-Anbieter müssen die **[MSProviderInit](msproviderinit.md)** -Funktion als Einstiegspunkt für die DLL des Anbieters initialisieren implementieren.</span><span class="sxs-lookup"><span data-stu-id="8f483-114">All wrapped PST store providers must implement the **[MSProviderInit](msproviderinit.md)** function as an entry point to initialize the provider's DLL.</span></span> <span data-ttu-id="8f483-115">**MSProviderInit** überprüft, ob die Versionsnummer der Anbieterschnittstelle Service `ulMAPIVer`, ist kompatibel mit die aktuelle Versionsnummer `CURRENT_SPI_VERSION`.</span><span class="sxs-lookup"><span data-stu-id="8f483-115">**MSProviderInit** checks to see if the version number of the service provider interface,  `ulMAPIVer`, is compatible with the current version number,  `CURRENT_SPI_VERSION`.</span></span> <span data-ttu-id="8f483-116">Die Funktion speichert den MAPI-Speicher Management Routinen in die `g_lpAllocateBuffer`, `g_lpAllocateMore`, und `g_lpFreeBuffer` Parameter.</span><span class="sxs-lookup"><span data-stu-id="8f483-116">The function saves the MAPI memory management routines into the  `g_lpAllocateBuffer`,  `g_lpAllocateMore`, and  `g_lpFreeBuffer` parameters.</span></span> <span data-ttu-id="8f483-117">Diese Speicher Management Routinen sollte während der gesamten Implementierung gepackten PST-Speicher für die Zuweisung von Arbeitsspeicher und Freigabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f483-117">These memory management routines should be used throughout the wrapped PST store implementation for memory allocation and deallocation.</span></span> 
  
### <a name="msproviderinit-example"></a><span data-ttu-id="8f483-118">MSProviderInit()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8f483-118">MSProviderInit() example</span></span>

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

### <a name="wrapped-pst-and-unicode-paths"></a><span data-ttu-id="8f483-119">Gepackten PST- und Unicode-Pfade</span><span class="sxs-lookup"><span data-stu-id="8f483-119">Wrapped PST and Unicode paths</span></span>

<span data-ttu-id="8f483-120">Um das ursprüngliche Beispiel in Microsoft Visual Studio 2008 Verwendung von Unicode-Pfade zum NST für die Verwendung in Unicode-aktivierten Microsoft Outlook 2010 und Outlook 2013 vorbereitete überarbeiten, sollten die **CreateStoreEntryID** -Routine, die die Eintrags-ID erstellt, das verwenden. ein Format für die ASCII-Pfade und ein weiteres für Unicode-Pfade.</span><span class="sxs-lookup"><span data-stu-id="8f483-120">To retrofit the original sample prepared in Microsoft Visual Studio 2008 to use Unicode paths to the NST for use in Unicode-enabled Microsoft Outlook 2010 and Outlook 2013, the **CreateStoreEntryID** routine, which produces the entry identifier, should use one format for ASCII paths, and another for Unicode paths.</span></span> <span data-ttu-id="8f483-121">Diese werden als Strukturen im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8f483-121">These are represented as structures in the following example.</span></span> 
  
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
> <span data-ttu-id="8f483-122">Die Unterschiede zwischen diesen Strukturen sind zwei NULL-Bytes vor einem Unicode-Pfad.</span><span class="sxs-lookup"><span data-stu-id="8f483-122">The differences in these structures are two NULL bytes prior to a Unicode path.</span></span> <span data-ttu-id="8f483-123">Wenn Sie interpretiert die Eintrags-ID in der "Service Eintrag routinemäßige", der die befolgt werden müssen, wäre eine Möglichkeit zum bestimmen, ob dies der Fall ist, wandeln Sie wie EIDMS zuerst, überprüfen Sie, ob die SzPath [0] NULL ist.</span><span class="sxs-lookup"><span data-stu-id="8f483-123">If you need to interpret the entry identifier in the "Service Entry Routine" that follows, one way to determine whether that is the case or not would be to cast as EIDMS first, then check whether the szPath[0] is NULL.</span></span> <span data-ttu-id="8f483-124">Es ist, stattdessen als EIDMSW umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="8f483-124">If it is, cast it as EIDMSW instead.</span></span> 
  
## <a name="service-entry-routine"></a><span data-ttu-id="8f483-125">Diensteintrag routine</span><span class="sxs-lookup"><span data-stu-id="8f483-125">Service Entry routine</span></span>

<span data-ttu-id="8f483-126">Die **[MSGSERVICEENTRY](msgserviceentry.md)** -Funktion ist der Einstiegspunkt des Nachricht, in der gepackten PST Informationsdienst konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="8f483-126">The **[MSGSERVICEENTRY](msgserviceentry.md)** function is the message service entry point where the wrapped PST store provider is configured.</span></span> <span data-ttu-id="8f483-127">Die Funktionsaufrufe `GetMemAllocRoutines()` an den MAPI-Speicher Management Routinen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8f483-127">The function calls  `GetMemAllocRoutines()` to get the MAPI memory management routines.</span></span> <span data-ttu-id="8f483-128">Die Funktion verwendet die `lpProviderAdmin` Parameter Abschnitts Profile für den Anbieter und legt die Eigenschaften im Benutzerprofil zu finden.</span><span class="sxs-lookup"><span data-stu-id="8f483-128">The function uses the  `lpProviderAdmin` parameter to locate the profile section for the provider and sets the properties in the profile.</span></span> 
  
### <a name="serviceentry-example"></a><span data-ttu-id="8f483-129">ServiceEntry()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8f483-129">ServiceEntry() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="8f483-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f483-130">See also</span></span>

- [<span data-ttu-id="8f483-131">Informationen über das Beispiel für einen Anbieter von umschlossenem PST-Speicher</span><span class="sxs-lookup"><span data-stu-id="8f483-131">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="8f483-132">Installieren des Beispiel für einen Anbieter von umschlossenem PST-Speicher</span><span class="sxs-lookup"><span data-stu-id="8f483-132">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="8f483-133">Anmelden bei einem Anbieter von umschlossenem PST-Speicher</span><span class="sxs-lookup"><span data-stu-id="8f483-133">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="8f483-134">Verwenden eines Anbieters von umschlossenem PST-Speicher</span><span class="sxs-lookup"><span data-stu-id="8f483-134">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="8f483-135">Herunterfahren eines Anbieters von umschlossenem PST-Speicher</span><span class="sxs-lookup"><span data-stu-id="8f483-135">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

