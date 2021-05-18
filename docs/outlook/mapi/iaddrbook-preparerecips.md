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
ms.openlocfilehash: db1c23f33e604d6aafdd8a046566c7390c281ad8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414277"
---
# <a name="iaddrbookpreparerecips"></a><span data-ttu-id="77d85-103">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="77d85-103">IAddrBook::PrepareRecips</span></span>

  
  
<span data-ttu-id="77d85-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77d85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77d85-105">Bereitet eine Empfängerliste für die spätere Verwendung durch das Messagingsystem vor.</span><span class="sxs-lookup"><span data-stu-id="77d85-105">Prepares a recipient list for later use by the messaging system.</span></span> 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="77d85-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="77d85-106">Parameters</span></span>

 <span data-ttu-id="77d85-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="77d85-107">_ulFlags_</span></span>
  
> <span data-ttu-id="77d85-108">[in] Eine Bitmaske mit Flags, die steuert, wie der Eintrag geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="77d85-108">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="77d85-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="77d85-109">The following flag can be set:</span></span>
    
<span data-ttu-id="77d85-110">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="77d85-110">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="77d85-111">Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="77d85-111">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="77d85-112">Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung das Öffnen der globalen Adressliste (GLOBAL Address List, GAL) im zwischengespeicherten Exchange-Modus und den Zugriff auf einen Eintrag in diesem Adressbuch aus dem Cache zu ermöglichen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="77d85-112">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and to access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="77d85-113">Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.</span><span class="sxs-lookup"><span data-stu-id="77d85-113">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="77d85-114">_lpSPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="77d85-114">_lpSPropTagArray_</span></span>
  
> <span data-ttu-id="77d85-115">[in] Ein Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die die Eigenschaften angeben, falls vorhanden, die aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="77d85-115">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties, if any, that require updating.</span></span> <span data-ttu-id="77d85-116">Der  _lpSPropTagArray-Parameter_ kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="77d85-116">The  _lpSPropTagArray_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="77d85-117">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="77d85-117">_lpRecipList_</span></span>
  
> <span data-ttu-id="77d85-118">[in] Ein Zeiger auf eine [ADRLIST-Struktur,](adrlist.md) die die Liste der Empfänger enthält.</span><span class="sxs-lookup"><span data-stu-id="77d85-118">[in] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="77d85-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77d85-119">Return value</span></span>

<span data-ttu-id="77d85-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="77d85-120">S_OK</span></span> 
  
> <span data-ttu-id="77d85-121">Die Empfängerliste wurde erfolgreich vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="77d85-121">The recipient list was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="77d85-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="77d85-122">Remarks</span></span>

<span data-ttu-id="77d85-123">Clients und Dienstanbieter rufen die **PrepareRecips-Methode** auf, um folgendes zu tun:</span><span class="sxs-lookup"><span data-stu-id="77d85-123">Clients and service providers call the **PrepareRecips** method to do the following:</span></span> 
  
- <span data-ttu-id="77d85-124">Stellen Sie sicher, dass alle Empfänger im  _lpRecipList-Parameter_ über langfristige Eintragsbezeichner verfügen.</span><span class="sxs-lookup"><span data-stu-id="77d85-124">Ensure that all recipients in the  _lpRecipList_ parameter have long-term entry identifiers.</span></span> 
    
- <span data-ttu-id="77d85-125">Stellen Sie sicher, dass jeder Empfänger im  _lpRecipList-Parameter_ über die im  _lpSPropTagArray-Parameter_ aufgeführten Eigenschaften verfügt und dass diese Eigenschaften am Anfang der Empfängerliste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="77d85-125">Ensure that each recipient in the  _lpRecipList_ parameter has the properties listed in the  _lpSPropTagArray_ parameter and that these properties appear at the start of the recipient list.</span></span> 
    
<span data-ttu-id="77d85-126">MAPI konvertiert die kurzfristigen Eintragsbezeichner jedes Empfängers in langfristige Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="77d85-126">MAPI converts each recipient's short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="77d85-127">Bei Bedarf werden die langfristigen Eintrags-IDs der Empfänger vom entsprechenden Adressbuchanbieter abgerufen, und es werden zusätzliche Eigenschaften angefordert.</span><span class="sxs-lookup"><span data-stu-id="77d85-127">If necessary, recipients' long-term entry identifiers are retrieved from the appropriate address book provider and any additional properties are requested.</span></span>
  
<span data-ttu-id="77d85-128">In einem einzelnen Empfängereintrag werden die angeforderten Eigenschaften zuerst geordnet, gefolgt von allen Eigenschaften, die bereits für den Eintrag vorhanden waren.</span><span class="sxs-lookup"><span data-stu-id="77d85-128">In an individual recipient entry, the requested properties are ordered first, followed by any properties that were already present for the entry.</span></span> <span data-ttu-id="77d85-129">Wenn eine oder mehrere der angeforderten Eigenschaften im  _lpSPropTagArray-Parameter_ nicht vom entsprechenden Adressbuchanbieter verarbeitet werden, werden ihre Eigenschaftstypen auf PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="77d85-129">If one or more of the requested properties in the  _lpSPropTagArray_ parameter are not handled by the appropriate address book provider, their property types will be set to PT_ERROR.</span></span> <span data-ttu-id="77d85-130">Ihre Eigenschaftswerte werden entweder auf MAPI_E_NOT_FOUND oder auf einen anderen Wert festgelegt, der einen genaueren Grund dafür gibt, warum die Eigenschaften nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="77d85-130">Their property values will be set to either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason why the properties are not available.</span></span> <span data-ttu-id="77d85-131">Jede im _lpRecipList-Parameter_ enthaltene [SPropValue-Struktur](spropvalue.md) muss mithilfe der [Funktionen MAPIAllocateBuffer](mapiallocatebuffer.md) und [MAPIAllocateMore](mapiallocatemore.md) separat zugeordnet werden, damit sie einzeln frei werden kann.</span><span class="sxs-lookup"><span data-stu-id="77d85-131">Each [SPropValue](spropvalue.md) structure included in the  _lpRecipList_ parameter must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions so that it can be freed individually.</span></span> 
  
<span data-ttu-id="77d85-132">Weitere Informationen zu PT_ERROR finden Sie unter [Property Types](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="77d85-132">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="77d85-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77d85-133">See also</span></span>



[<span data-ttu-id="77d85-134">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="77d85-134">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="77d85-135">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="77d85-135">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="77d85-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="77d85-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="77d85-137">PidTagEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="77d85-137">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="77d85-138">SPropValue</span><span class="sxs-lookup"><span data-stu-id="77d85-138">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="77d85-139">SRowSet</span><span class="sxs-lookup"><span data-stu-id="77d85-139">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="77d85-140">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="77d85-140">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

