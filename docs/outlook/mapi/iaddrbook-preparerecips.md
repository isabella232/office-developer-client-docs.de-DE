---
title: IAddrBookPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.PrepareRecips
api_type:
- COM
ms.assetid: d423f7b5-23b8-44dd-bca3-6590182dc42d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fe3e098b2b70e77bd0c536002a4724810261bff3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19792028"
---
# <a name="iaddrbookpreparerecips"></a><span data-ttu-id="b052a-103">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="b052a-103">IAddrBook::PrepareRecips</span></span>

  
  
<span data-ttu-id="b052a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b052a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b052a-105">Bereitet eine Empfängerliste zur späteren Verwendung von messaging-System.</span><span class="sxs-lookup"><span data-stu-id="b052a-105">Prepares a recipient list for later use by the messaging system.</span></span> 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="b052a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b052a-106">Parameters</span></span>

 <span data-ttu-id="b052a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b052a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b052a-108">[in] Eine Bitmaske aus Flags, die steuert, wie der Eintrag geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="b052a-108">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="b052a-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b052a-109">The following flag can be set:</span></span>
    
<span data-ttu-id="b052a-110">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="b052a-110">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="b052a-111">Verwenden Sie nur das Offlineadressbuch, um namensauflösung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b052a-111">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="b052a-112">Dieses Kennzeichen können Sie beispielsweise um eine Clientanwendung aus die globalen Adressliste (GAL) im Exchange-Cache-Modus geöffnet und den Zugriff auf eines Eintrags in diesem Adressbuch aus dem Cache ohne Erstellen von Datenverkehr zwischen dem Client und dem Server zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b052a-112">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and to access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="b052a-113">Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b052a-113">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="b052a-114">_lpSPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="b052a-114">_lpSPropTagArray_</span></span>
  
> <span data-ttu-id="b052a-115">[in] Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Eigenschaftentags enthält, die die Eigenschaften gegebenenfalls hinweisen, Aktualisierung erfordern.</span><span class="sxs-lookup"><span data-stu-id="b052a-115">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties, if any, that require updating.</span></span> <span data-ttu-id="b052a-116">Der Parameter _LpSPropTagArray_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b052a-116">The  _lpSPropTagArray_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="b052a-117">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="b052a-117">_lpRecipList_</span></span>
  
> <span data-ttu-id="b052a-118">[in] Ein Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die die Liste der Empfänger enthält.</span><span class="sxs-lookup"><span data-stu-id="b052a-118">[in] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b052a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b052a-119">Return value</span></span>

<span data-ttu-id="b052a-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="b052a-120">S_OK</span></span> 
  
> <span data-ttu-id="b052a-121">Die Empfängerliste wurde erfolgreich vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="b052a-121">The recipient list was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b052a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b052a-122">Remarks</span></span>

<span data-ttu-id="b052a-123">Clients und Dienstanbieter rufen Sie die **PrepareRecips** -Methode, um Folgendes auszuführen:</span><span class="sxs-lookup"><span data-stu-id="b052a-123">Clients and service providers call the **PrepareRecips** method to do the following:</span></span> 
  
- <span data-ttu-id="b052a-124">Stellen Sie sicher, dass alle Empfänger im Parameter _LpRecipList_ langfristige-Eintragsbezeichner verfügen.</span><span class="sxs-lookup"><span data-stu-id="b052a-124">Ensure that all recipients in the  _lpRecipList_ parameter have long-term entry identifiers.</span></span> 
    
- <span data-ttu-id="b052a-125">Stellen Sie sicher, dass der Empfänger in der _LpRecipList_ -Parameter im Parameter _LpSPropTagArray_ aufgeführten Eigenschaften verfügt und dass diese Eigenschaften am Anfang der Empfängerliste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b052a-125">Ensure that each recipient in the  _lpRecipList_ parameter has the properties listed in the  _lpSPropTagArray_ parameter and that these properties appear at the start of the recipient list.</span></span> 
    
<span data-ttu-id="b052a-126">MAPI konvertiert des Empfängers kurzfristige-Eintragsbezeichner langfristige-Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="b052a-126">MAPI converts each recipient's short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="b052a-127">Gegebenenfalls Empfänger langfristige-Eintragsbezeichner aus der entsprechenden Adressbuchanbieter abgerufen werden, und alle zusätzlichen Eigenschaften angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="b052a-127">If necessary, recipients' long-term entry identifiers are retrieved from the appropriate address book provider and any additional properties are requested.</span></span>
  
<span data-ttu-id="b052a-128">In einen einzelnen Empfänger Eintrag werden Sie zunächst die angeforderten Eigenschaften sortiert gefolgt von Eigenschaften, die bereits für den Eintrag vorhanden waren.</span><span class="sxs-lookup"><span data-stu-id="b052a-128">In an individual recipient entry, the requested properties are ordered first, followed by any properties that were already present for the entry.</span></span> <span data-ttu-id="b052a-129">Wenn eine oder mehrere der angeforderten Eigenschaften im _LpSPropTagArray_ -Parameter nicht durch die entsprechende Adressbuchanbieter behandelt werden, werden ihre Eigenschaftentypen auf PT_ERROR festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b052a-129">If one or more of the requested properties in the  _lpSPropTagArray_ parameter are not handled by the appropriate address book provider, their property types will be set to PT_ERROR.</span></span> <span data-ttu-id="b052a-130">Die Eigenschaftswerte werden festgelegt werden MAPI_E_NOT_FOUND oder auf einen anderen Wert, der einen genauere Grund gibt, warum die Eigenschaften nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b052a-130">Their property values will be set to either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason why the properties are not available.</span></span> <span data-ttu-id="b052a-131">Jede [SPropValue](spropvalue.md) -Struktur, die in der _LpRecipList_ -Parameter enthalten muss separat zugeordnet werden, mithilfe der Funktionen [MAPIAllocateBuffer](mapiallocatebuffer.md) und [MAPIAllocateMore](mapiallocatemore.md) , damit er einzeln freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="b052a-131">Each [SPropValue](spropvalue.md) structure included in the  _lpRecipList_ parameter must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions so that it can be freed individually.</span></span> 
  
<span data-ttu-id="b052a-132">Informationen zu PT_ERROR finden Sie unter [Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="b052a-132">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b052a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b052a-133">See also</span></span>



[<span data-ttu-id="b052a-134">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="b052a-134">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="b052a-135">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="b052a-135">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="b052a-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="b052a-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="b052a-137">PidTagEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b052a-137">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="b052a-138">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b052a-138">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="b052a-139">SRowSet</span><span class="sxs-lookup"><span data-stu-id="b052a-139">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="b052a-140">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b052a-140">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

