---
title: Anmelden bei einem Anbieter von umschlossenem PST-Speicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Letzte Änderung: 02. Juli 2012'
ms.openlocfilehash: 96f472d67f144a451046ff61a3ed6c6ff2ff9acf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408986"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a><span data-ttu-id="b441b-103">Anmelden bei einem Anbieter von umschlossenem PST-Speicher</span><span class="sxs-lookup"><span data-stu-id="b441b-103">Logging on to a wrapped PST store provider</span></span>

<span data-ttu-id="b441b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b441b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b441b-105">Bevor Sie sich bei mapI bei einem umschlossenen ANBIETER für den PST-Speicher anmelden können, müssen Sie den umschlossenen Anbieter für persönliche Ordner (PST) initialisieren und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b441b-105">Before you can log on MAPI to a wrapped PST store provider, you must initialize and configure the wrapped Personal Folders file (PST) store provider.</span></span> <span data-ttu-id="b441b-106">Weitere Informationen finden Sie unter [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b441b-106">For more information, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="b441b-107">Nachdem Sie einen umschlossenen PST Store-Anbieter initialisiert und konfiguriert haben, müssen Sie zwei Anmelderoutinen implementieren.</span><span class="sxs-lookup"><span data-stu-id="b441b-107">After you have initialized and configured a wrapped PST store provider, you must implement two logon routines.</span></span> <span data-ttu-id="b441b-108">Die **[IMSProvider::Logon-Funktion](imsprovider-logon.md)** meldet sich auf MAPI an den umschlossenen ANBIETER des PST-Speichers.</span><span class="sxs-lookup"><span data-stu-id="b441b-108">The **[IMSProvider::Logon](imsprovider-logon.md)** function logs on MAPI to the wrapped PST store provider.</span></span> <span data-ttu-id="b441b-109">Die **[IMSProvider::SpoolerLogon-Funktion](imsprovider-spoolerlogon.md)** protokolliert im MAPI-Spooler an den umschlossenen PST-Speicheranbieter.</span><span class="sxs-lookup"><span data-stu-id="b441b-109">The **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function logs on the MAPI spooler to the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="b441b-110">In diesem Thema werden die **IMSProvider::Logon-Funktion** und die **IMSProvider::SpoolerLogon-Funktion** anhand von Codebeispielen aus dem Beispiel umschlossenen PST Store demonstriert.</span><span class="sxs-lookup"><span data-stu-id="b441b-110">In this topic, the **IMSProvider::Logon** function and the **IMSProvider::SpoolerLogon** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="b441b-111">Das Beispiel implementiert einen umschlossenen PST-Anbieter, der in Verbindung mit der Replikations-API verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b441b-111">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="b441b-112">Weitere Informationen zum Herunterladen und Installieren des Beispielanbieters für umbrochene PST Store finden Sie unter [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b441b-112">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="b441b-113">Weitere Informationen zur Replikations-API finden Sie unter [Informationen zur Replikations-API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="b441b-113">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="b441b-114">Nachdem MAPI und der MAPI-Spooler beim umschlossenen ANBIETER für den PST Store angemeldet sind, kann er verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b441b-114">After MAPI and the MAPI spooler are logged on to the wrapped PST store provider, it is ready to be used.</span></span> <span data-ttu-id="b441b-115">Weitere Informationen finden Sie unter [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b441b-115">For more information, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="mapi-logon-routine"></a><span data-ttu-id="b441b-116">MAPI-Anmelderoutine</span><span class="sxs-lookup"><span data-stu-id="b441b-116">MAPI Logon routine</span></span>

<span data-ttu-id="b441b-117">Nachdem der umschlossene ANBIETER für den PST-Speicher initialisiert wurde, müssen Sie die **[IMSProvider::Logon-Funktion](imsprovider-logon.md)** implementieren, um mapI beim umschlossenen PST-Speicher zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="b441b-117">After the wrapped PST store provider is initialized, you must implement the **[IMSProvider::Logon](imsprovider-logon.md)** function to log on MAPI to the wrapped PST store.</span></span> <span data-ttu-id="b441b-118">Diese Funktion überprüft Benutzeranmeldeinformationen und ruft die Konfigurationseigenschaften für den Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="b441b-118">This function validates user credentials and gets the configuration properties for the provider.</span></span> <span data-ttu-id="b441b-119">Sie müssen auch die Funktion `SetOLFIInOST` implementieren, um die Offlinedateiinformationen ( OLFI )**[festlegen zu können.](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="b441b-119">You must also implement the  `SetOLFIInOST` function to set the Offline File Info (**[OLFI](olfi.md)** ).</span></span> <span data-ttu-id="b441b-120">**OLFI** ist eine Warteschlange mit langfristigen ID-Strukturen, die vom umschlossenen Pst Store-Anbieter zum Zuweisen einer Eintrags-ID für eine neue Nachricht oder einen neuen Ordner im Offlinemodus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b441b-120">**OLFI** is a queue of long-term ID structures that is used by the wrapped PST store provider to assign an Entry ID for a new message or folder in offline mode.</span></span> <span data-ttu-id="b441b-121">Schließlich gibt die **IMSProvider::Logon-Funktion** ein Nachrichtenspeicherobjekt zurück, an das sich der MAPI-Spooler und die Clientanwendungen im Parameter anmelden  `ppMDB` können.</span><span class="sxs-lookup"><span data-stu-id="b441b-121">Finally, the **IMSProvider::Logon** function returns a message store object that the MAPI spooler and client applications can log on to in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderlogon-example"></a><span data-ttu-id="b441b-122">CMSProvider::Logon()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="b441b-122">CMSProvider::Logon() example</span></span>

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

## <a name="mapi-spooler-logon-routine"></a><span data-ttu-id="b441b-123">MAPI-Spooler-Anmelderoutine</span><span class="sxs-lookup"><span data-stu-id="b441b-123">MAPI Spooler Logon routine</span></span>

<span data-ttu-id="b441b-124">Ähnlich wie **IMSProvider::Logon** müssen Sie die **[IMSProvider::SpoolerLogon-Funktion](imsprovider-spoolerlogon.md)** implementieren, um den MAPI-Spooler im umschlossenen PST-Speicher zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="b441b-124">Similar to **IMSProvider::Logon**, you must implement the **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function to log the MAPI spooler on to the wrapped PST store.</span></span> <span data-ttu-id="b441b-125">Ein Nachrichtenspeicherobjekt, an dem sich der MAPI-Spooler und die Clientanwendungen anmelden können, wird im Parameter  `ppMDB` zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b441b-125">A message store object that the MAPI spooler and client applications can log on to is returned in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderspoolerlogon-example"></a><span data-ttu-id="b441b-126">CMSProvider::SpoolerLogon()-Beispiel</span><span class="sxs-lookup"><span data-stu-id="b441b-126">CMSProvider::SpoolerLogon() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="b441b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b441b-127">See also</span></span>

- [<span data-ttu-id="b441b-128">Informationen zum Beispiel umschlossenen STORE Anbieter</span><span class="sxs-lookup"><span data-stu-id="b441b-128">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="b441b-129">Installieren des Umschlossenen Store -Beispielanbieters</span><span class="sxs-lookup"><span data-stu-id="b441b-129">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="b441b-130">Initialisieren eines umschlossenen STORE Anbieters</span><span class="sxs-lookup"><span data-stu-id="b441b-130">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="b441b-131">Verwenden eines umschlossenen STORE Anbieters</span><span class="sxs-lookup"><span data-stu-id="b441b-131">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="b441b-132">Herunterfahren eines umschlossenen STORE Anbieters</span><span class="sxs-lookup"><span data-stu-id="b441b-132">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

