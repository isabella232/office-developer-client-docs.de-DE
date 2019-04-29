---
title: Anmelden bei einem Anbieter von umschlossenem PST-Speicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Zuletzt geändert: 02 Juli, 2012'
ms.openlocfilehash: 96f472d67f144a451046ff61a3ed6c6ff2ff9acf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408986"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a><span data-ttu-id="a6d73-103">Anmelden bei einem Anbieter von umschlossenem PST-Speicher</span><span class="sxs-lookup"><span data-stu-id="a6d73-103">Logging on to a wrapped PST store provider</span></span>

<span data-ttu-id="a6d73-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6d73-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6d73-105">Bevor Sie MAPI bei einem eingebundenen PST-Speicheranbieter anmelden können, müssen Sie den eingebundenen PST-Speicheranbieter initialisieren und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a6d73-105">Before you can log on MAPI to a wrapped PST store provider, you must initialize and configure the wrapped Personal Folders file (PST) store provider.</span></span> <span data-ttu-id="a6d73-106">Weitere Informationen finden Sie unter [Initialisieren eines EingebundenEN PST-Speicheranbieters](initializing-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a6d73-106">For more information, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="a6d73-107">Nachdem Sie einen eingebundenen PST-Speicheranbieter initialisiert und konfiguriert haben, müssen Sie zwei Anmelde Routinen implementieren.</span><span class="sxs-lookup"><span data-stu-id="a6d73-107">After you have initialized and configured a wrapped PST store provider, you must implement two logon routines.</span></span> <span data-ttu-id="a6d73-108">Die **[IMSProvider:: LOGON](imsprovider-logon.md)** -Funktion meldet MAPI für den eingebundenen PST-Speicheranbieter an.</span><span class="sxs-lookup"><span data-stu-id="a6d73-108">The **[IMSProvider::Logon](imsprovider-logon.md)** function logs on MAPI to the wrapped PST store provider.</span></span> <span data-ttu-id="a6d73-109">Die **[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)** -Funktion meldet den MAPI-Spooler für den eingebundenen PST-Speicheranbieter an.</span><span class="sxs-lookup"><span data-stu-id="a6d73-109">The **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function logs on the MAPI spooler to the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="a6d73-110">In diesem Thema werden die **IMSProvider:: LOGON** -Funktion und die **IMSProvider:: SpoolerLogon** -Funktion mithilfe von Codebeispielen aus dem beispielsWEISE einGebundenen PST-Speicheranbieter demonstriert.</span><span class="sxs-lookup"><span data-stu-id="a6d73-110">In this topic, the **IMSProvider::Logon** function and the **IMSProvider::SpoolerLogon** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="a6d73-111">Im Beispiel wird ein eingebundener PST-Anbieter implementiert, der in Verbindung mit der Replikations-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6d73-111">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="a6d73-112">Weitere Informationen zum herunterladen und Installieren des eingeWickelten Beispiel-PST-Speicheranbieters finden Sie unter [Installing the Sample Wrapped Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a6d73-112">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="a6d73-113">Weitere Informationen zur Replikations-API finden Sie unter Informationen zur [Replikations-API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="a6d73-113">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="a6d73-114">Nachdem MAPI und der MAPI-Spooler beim eingebundenen PST-Speicheranbieter angemeldet sind, können Sie diese verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6d73-114">After MAPI and the MAPI spooler are logged on to the wrapped PST store provider, it is ready to be used.</span></span> <span data-ttu-id="a6d73-115">Weitere Informationen finden Sie unter [Verwenden eines EingebundenEN PST-Speicheranbieters](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a6d73-115">For more information, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="mapi-logon-routine"></a><span data-ttu-id="a6d73-116">MAPI-Anmelderoutine</span><span class="sxs-lookup"><span data-stu-id="a6d73-116">MAPI Logon routine</span></span>

<span data-ttu-id="a6d73-117">Nachdem der eingebundene PST-Speicheranbieter initialisiert wurde, müssen Sie die **[IMSProvider:: LOGON](imsprovider-logon.md)** -Funktion implementieren, um sich bei MAPI im eingebundenen PST-Speicher anzumelden.</span><span class="sxs-lookup"><span data-stu-id="a6d73-117">After the wrapped PST store provider is initialized, you must implement the **[IMSProvider::Logon](imsprovider-logon.md)** function to log on MAPI to the wrapped PST store.</span></span> <span data-ttu-id="a6d73-118">Diese Funktion überprüft Benutzeranmeldeinformationen und ruft die Konfigurationseigenschaften für den Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="a6d73-118">This function validates user credentials and gets the configuration properties for the provider.</span></span> <span data-ttu-id="a6d73-119">Sie müssen auch die `SetOLFIInOST` Funktion zum Festlegen der Offline Datei Info (**[OLFI](olfi.md)** ) implementieren.</span><span class="sxs-lookup"><span data-stu-id="a6d73-119">You must also implement the  `SetOLFIInOST` function to set the Offline File Info (**[OLFI](olfi.md)** ).</span></span> <span data-ttu-id="a6d73-120">**OLFI** ist eine Warteschlange von langfristigen ID-Strukturen, die vom eingebundenen PST-Speicheranbieter zum Zuweisen einer EINTRAGS-ID für eine neue Nachricht oder einen neuen Ordner im Offlinemodus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a6d73-120">**OLFI** is a queue of long-term ID structures that is used by the wrapped PST store provider to assign an Entry ID for a new message or folder in offline mode.</span></span> <span data-ttu-id="a6d73-121">Schließlich gibt die **IMSProvider:: LOGON** -Funktion ein Nachrichtenspeicherobjekt zurück, das von der MAPI-Spooler-und der Client `ppMDB` Anwendung im Parameter angemeldet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a6d73-121">Finally, the **IMSProvider::Logon** function returns a message store object that the MAPI spooler and client applications can log on to in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderlogon-example"></a><span data-ttu-id="a6d73-122">CMSProvider:: LOGON () (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="a6d73-122">CMSProvider::Logon() example</span></span>

```cpp
STDMETHODIMP CMSProvider::Logon( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG * pcbSpoolSecurity, 
    LPBYTE * ppbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
    LPMDB lpPSTMDB = NULL; 
    CMsgStore* pWrappedMDB = NULL; 
 
    Log(true,"CMSProvider::Logon Pst logon Called\n"); 
 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        ulFlags = (ulFlags & ~MDB_OST_LOGON_ANSI) | MDB_OST_LOGON_UNICODE; 
        hRes = m_pPSTMS->Logon( 
            pMySup, 
            ulUIParam,  
            pszProfileName,  
            cbEntryID, 
            pEntryID,  
            ulFlags,  
            pInterface,  
            pcbSpoolSecurity, 
            ppbSpoolSecurity,  
            ppMAPIError,  
            ppMSLogon,  
            &lpPSTMDB); 
    } 
    Log(true,"CMSProvider::Logon returned 0x%08X\n", hRes); 
 
    // Set up the MDB to allow synchronization 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = SetOLFIInOST(lpPSTMDB); 
        Log(true,"SetOLFIInOST returned 0x%08X\n", hRes); 
    } 
    // Wrap the outgoing MDB 
    pWrappedMDB = new CMsgStore (lpPSTMDB); 
    if (NULL == pWrappedMDB) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CMsgStore object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    // Copy pointer to the allocated object back into the return LPMDB object pointer 
    *ppMDB = pWrappedMDB; 
    if (lpProfSect) lpProfSect->Release(); 
 
    return hRes; 
}
```

## <a name="mapi-spooler-logon-routine"></a><span data-ttu-id="a6d73-123">MAPI-Spooler-Anmelderoutine</span><span class="sxs-lookup"><span data-stu-id="a6d73-123">MAPI Spooler Logon routine</span></span>

<span data-ttu-id="a6d73-124">Ähnlich wie **IMSProvider:: LOGON**müssen Sie die **[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)** -Funktion implementieren, um den MAPI-Spooler für den eingebundenen PST-Speicher zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="a6d73-124">Similar to **IMSProvider::Logon**, you must implement the **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function to log the MAPI spooler on to the wrapped PST store.</span></span> <span data-ttu-id="a6d73-125">Ein Nachrichtenspeicherobjekt, an das sich die MAPI-Warteschlange und die Clientanwendungen anmelden können, `ppMDB` wird im-Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a6d73-125">A message store object that the MAPI spooler and client applications can log on to is returned in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderspoolerlogon-example"></a><span data-ttu-id="a6d73-126">CMSProvider:: SpoolerLogon ()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="a6d73-126">CMSProvider::SpoolerLogon() example</span></span>

```cpp
STDMETHODIMP CMSProvider::SpoolerLogon ( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG cbSpoolSecurity, 
    LPBYTE pbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
     
    Log(true,"CMSProvider::SpoolerLogon\n"); 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::SpoolerLogon: " + 
            "Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = m_pPSTMS->SpoolerLogon(  
            pMySup,//pSupObj, 
            ulUIParam, 
            pszProfileName, 
            cbEntryID, 
            pEntryID, 
            ulFlags, 
            pInterface, 
            cbSpoolSecurity, 
            pbSpoolSecurity, 
            ppMAPIError, 
            ppMSLogon, 
            ppMDB); 
    } 
    Log(true,"CMSProvider::SpoolerLogon returned 0x%08X\n", hRes); 
 
    return hRes; 
}
```

## <a name="see-also"></a><span data-ttu-id="a6d73-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6d73-127">See also</span></span>

- [<span data-ttu-id="a6d73-128">Informationen zum einGebundenen PST-Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="a6d73-128">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="a6d73-129">Installieren des eingeWickelten Beispiel-PST-Speicheranbieters</span><span class="sxs-lookup"><span data-stu-id="a6d73-129">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="a6d73-130">Initialisieren eines einGebundenen PST-Speicheranbieters</span><span class="sxs-lookup"><span data-stu-id="a6d73-130">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="a6d73-131">Verwenden eines einGebundenen PST-Speicheranbieters</span><span class="sxs-lookup"><span data-stu-id="a6d73-131">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="a6d73-132">Herunterfahren eines einGebundenen PST-Speicheranbieters</span><span class="sxs-lookup"><span data-stu-id="a6d73-132">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

