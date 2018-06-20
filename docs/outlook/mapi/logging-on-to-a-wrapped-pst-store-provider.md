---
title: Anmelden bei einem gepackten PST-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Zuletzt geändert: 02 Juli 2012'
ms.openlocfilehash: 2dfa3820d8d2ab57f278e90bef5d5a40164da6fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792893"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a><span data-ttu-id="f5139-103">Anmelden bei einem gepackten PST-Anbieter</span><span class="sxs-lookup"><span data-stu-id="f5139-103">Logging on to a wrapped PST store provider</span></span>

<span data-ttu-id="f5139-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f5139-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f5139-105">Bevor Sie zu einem gepackten PST-Speicher-Anbieter auf MAPI anmelden können, müssen Sie initialisieren und konfigurieren den gepackten Anbieter für Persönliche Ordner-Datei (PST) anmelden.</span><span class="sxs-lookup"><span data-stu-id="f5139-105">Before you can log on MAPI to a wrapped PST store provider, you must initialize and configure the wrapped Personal Folders file (PST) store provider.</span></span> <span data-ttu-id="f5139-106">Weitere Informationen finden Sie unter [einem umfließendem PST-Anbieter zu initialisieren](initializing-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f5139-106">For more information, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="f5139-107">Nachdem Sie initialisiert und einen gepackten PST-Anbieter konfiguriert haben, müssen Sie zwei Anmeldung Routinen implementieren.</span><span class="sxs-lookup"><span data-stu-id="f5139-107">After you have initialized and configured a wrapped PST store provider, you must implement two logon routines.</span></span> <span data-ttu-id="f5139-108">Die Funktion **[IMSProvider::Logon](imsprovider-logon.md)** anmeldet MAPI auf die gepackten PST-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="f5139-108">The **[IMSProvider::Logon](imsprovider-logon.md)** function logs on MAPI to the wrapped PST store provider.</span></span> <span data-ttu-id="f5139-109">Die Funktion **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** meldet sich die MAPI-Warteschlange auf dem gepackten PST-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="f5139-109">The **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function logs on the MAPI spooler to the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="f5139-110">In diesem Thema werden die **IMSProvider::Logon** und der **IMSProvider::SpoolerLogon** -Funktion mithilfe von Codebeispielen aus der umbrochen PST Store Beispielanbieter veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f5139-110">In this topic, the **IMSProvider::Logon** function and the **IMSProvider::SpoolerLogon** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="f5139-111">Das Beispiel implementiert einen gepackten PST-Anbieter, der in Verbindung mit der API für die Replikation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5139-111">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="f5139-112">Weitere Informationen zum Herunterladen und Installieren der umbrochen PST Store Beispielanbieter finden Sie unter [Sample umfließendem PST Store Provider installieren](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f5139-112">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="f5139-113">Weitere Informationen zur Replikation-API finden Sie unter [Über die Replikation-API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="f5139-113">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="f5139-114">Nachdem MAPI- und die MAPI-Warteschlange angemeldet sind bei der gepackten PST-Speicheranbieter ist, verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5139-114">After MAPI and the MAPI spooler are logged on to the wrapped PST store provider, it is ready to be used.</span></span> <span data-ttu-id="f5139-115">Weitere Informationen finden Sie unter [Verwenden von einem umfließendem PST-Anbieter](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f5139-115">For more information, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="mapi-logon-routine"></a><span data-ttu-id="f5139-116">MAPI-Anmeldung routine</span><span class="sxs-lookup"><span data-stu-id="f5139-116">MAPI Logon routine</span></span>

<span data-ttu-id="f5139-117">Nachdem der gepackten PST-Speicheranbieter initialisiert wurde, müssen Sie die **[IMSProvider::Logon](imsprovider-logon.md)** -Funktion zum Anmelden MAPI an den gepackten PST Store implementieren.</span><span class="sxs-lookup"><span data-stu-id="f5139-117">After the wrapped PST store provider is initialized, you must implement the **[IMSProvider::Logon](imsprovider-logon.md)** function to log on MAPI to the wrapped PST store.</span></span> <span data-ttu-id="f5139-118">Diese Funktion überprüft die Anmeldeinformationen und ruft die Konfigurationseigenschaften für den Anbieter.</span><span class="sxs-lookup"><span data-stu-id="f5139-118">This function validates user credentials and gets the configuration properties for the provider.</span></span> <span data-ttu-id="f5139-119">Sie müssen auch Implementieren der `SetOLFIInOST` -Funktion zum Festlegen der Offline Dateiinformationen (**[OLFI](olfi.md)** ).</span><span class="sxs-lookup"><span data-stu-id="f5139-119">You must also implement the  `SetOLFIInOST` function to set the Offline File Info (**[OLFI](olfi.md)** ).</span></span> <span data-ttu-id="f5139-120">**OLFI** ist eine Warteschlange der langfristigen ID Strukturen, die von der gepackten PST-Anbieter verwendet wird, weisen Sie eine Eintrags-ID für eine neue Nachricht oder einen Ordner im Offlinemodus.</span><span class="sxs-lookup"><span data-stu-id="f5139-120">**OLFI** is a queue of long-term ID structures that is used by the wrapped PST store provider to assign an Entry ID for a new message or folder in offline mode.</span></span> <span data-ttu-id="f5139-121">Schließlich gibt die Funktion **IMSProvider::Logon** ein Nachricht Store-Objekt, das die MAPI-Warteschlange und Clientanwendungen in anmelden können der `ppMDB` Parameter.</span><span class="sxs-lookup"><span data-stu-id="f5139-121">Finally, the **IMSProvider::Logon** function returns a message store object that the MAPI spooler and client applications can log on to in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderlogon-example"></a><span data-ttu-id="f5139-122">CMSProvider::Logon()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="f5139-122">CMSProvider::Logon() example</span></span>

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

## <a name="mapi-spooler-logon-routine"></a><span data-ttu-id="f5139-123">MAPI-Warteschlange Anmeldung routine</span><span class="sxs-lookup"><span data-stu-id="f5139-123">MAPI Spooler Logon routine</span></span>

<span data-ttu-id="f5139-124">Ähnlich wie **IMSProvider::Logon**, müssen Sie die **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** -Funktion, um die MAPI-Warteschlange an den gepackten PST-Speicher melden implementieren.</span><span class="sxs-lookup"><span data-stu-id="f5139-124">Similar to **IMSProvider::Logon**, you must implement the **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function to log the MAPI spooler on to the wrapped PST store.</span></span> <span data-ttu-id="f5139-125">Eine Nachricht Store-Objekt, das die MAPI-Warteschlange und Clientanwendungen anmelden können returned in der `ppMDB` Parameter.</span><span class="sxs-lookup"><span data-stu-id="f5139-125">A message store object that the MAPI spooler and client applications can log on to is returned in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderspoolerlogon-example"></a><span data-ttu-id="f5139-126">CMSProvider::SpoolerLogon()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="f5139-126">CMSProvider::SpoolerLogon() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="f5139-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5139-127">See also</span></span>

- [<span data-ttu-id="f5139-128">Zum Beispiel umgebrochen PST-Anbieter</span><span class="sxs-lookup"><span data-stu-id="f5139-128">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="f5139-129">Installieren des Beispiels umfließendem PST-Anbieter</span><span class="sxs-lookup"><span data-stu-id="f5139-129">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="f5139-130">Initialisieren einen Anbieter für umbrochenen PST anmelden</span><span class="sxs-lookup"><span data-stu-id="f5139-130">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="f5139-131">Verwenden eines Anbieters gepackten PST-Speichers</span><span class="sxs-lookup"><span data-stu-id="f5139-131">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="f5139-132">Herunterfahren von einem Anbieter gepackten PST-Datei</span><span class="sxs-lookup"><span data-stu-id="f5139-132">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

