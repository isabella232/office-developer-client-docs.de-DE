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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339221"
---
# <a name="iaddrbookpreparerecips"></a><span data-ttu-id="dc2a9-103">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="dc2a9-103">IAddrBook::PrepareRecips</span></span>

  
  
<span data-ttu-id="dc2a9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc2a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc2a9-105">Bereitet eine Empfängerliste für die spätere Verwendung durch das Messagingsystem vor.</span><span class="sxs-lookup"><span data-stu-id="dc2a9-105">Prepares a recipient list for later use by the messaging system.</span></span> 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="dc2a9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc2a9-106">Parameters</span></span>

 <span data-ttu-id="dc2a9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dc2a9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dc2a9-108">in Eine Bitmaske von Flags, die steuert, wie der Eintrag geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="dc2a9-108">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="dc2a9-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="dc2a9-109">The following flag can be set:</span></span>
    
<span data-ttu-id="dc2a9-110">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="dc2a9-110">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="dc2a9-111">Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="dc2a9-111">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="dc2a9-112">Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung das Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus zu gestatten und den Zugriff auf einen Eintrag in diesem Adressbuch aus dem Cache zu ermöglichen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dc2a9-112">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and to access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="dc2a9-113">Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc2a9-113">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="dc2a9-114">_lpSPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="dc2a9-114">_lpSPropTagArray_</span></span>
  
> <span data-ttu-id="dc2a9-115">in Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags enthält, die die Eigenschaften anzeigen, die aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="dc2a9-115">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties, if any, that require updating.</span></span> <span data-ttu-id="dc2a9-116">Der _lpSPropTagArray_ -Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="dc2a9-116">The  _lpSPropTagArray_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="dc2a9-117">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="dc2a9-117">_lpRecipList_</span></span>
  
> <span data-ttu-id="dc2a9-118">in Ein Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die die Liste der Empfänger enthält.</span><span class="sxs-lookup"><span data-stu-id="dc2a9-118">[in] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dc2a9-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc2a9-119">Return value</span></span>

<span data-ttu-id="dc2a9-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc2a9-120">S_OK</span></span> 
  
> <span data-ttu-id="dc2a9-121">Die Empfängerliste wurde erfolgreich vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="dc2a9-121">The recipient list was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc2a9-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc2a9-122">Remarks</span></span>

<span data-ttu-id="dc2a9-123">Clients und Dienstanbieter rufen die **PrepareRecips** -Methode auf, um folgende Aktionen auszuführen:</span><span class="sxs-lookup"><span data-stu-id="dc2a9-123">Clients and service providers call the **PrepareRecips** method to do the following:</span></span> 
  
- <span data-ttu-id="dc2a9-124">Stellen Sie sicher, dass alle Empfänger im Parameter _lpRecipList_ langfristige Eintragsbezeichner aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dc2a9-124">Ensure that all recipients in the  _lpRecipList_ parameter have long-term entry identifiers.</span></span> 
    
- <span data-ttu-id="dc2a9-125">Stellen Sie sicher, dass jeder Empfänger im _lpRecipList_ -Parameter über die im Parameter _lpSPropTagArray_ aufgeführten Eigenschaften verfügt und diese Eigenschaften am Anfang der Empfängerliste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="dc2a9-125">Ensure that each recipient in the  _lpRecipList_ parameter has the properties listed in the  _lpSPropTagArray_ parameter and that these properties appear at the start of the recipient list.</span></span> 
    
<span data-ttu-id="dc2a9-126">MAPI konvertiert die kurzfristigen Eintragsbezeichner der einzelnen Empfänger in langfristige Eintrags-IDs.</span><span class="sxs-lookup"><span data-stu-id="dc2a9-126">MAPI converts each recipient's short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="dc2a9-127">Bei Bedarf werden die langfristigen Eintragsbezeichner des Empfängers aus dem entsprechenden Adressbuchanbieter abgerufen, und zusätzliche Eigenschaften werden angefordert.</span><span class="sxs-lookup"><span data-stu-id="dc2a9-127">If necessary, recipients' long-term entry identifiers are retrieved from the appropriate address book provider and any additional properties are requested.</span></span>
  
<span data-ttu-id="dc2a9-128">In einem einzelnen Empfängereintrag werden die angeforderten Eigenschaften zuerst sortiert, gefolgt von Eigenschaften, die bereits für den Eintrag vorhanden waren.</span><span class="sxs-lookup"><span data-stu-id="dc2a9-128">In an individual recipient entry, the requested properties are ordered first, followed by any properties that were already present for the entry.</span></span> <span data-ttu-id="dc2a9-129">Wenn eine oder mehrere der angeforderten Eigenschaften im _lpSPropTagArray_ -Parameter nicht vom entsprechenden Adressbuchanbieter verarbeitet werden, werden Ihre Eigenschaftentypen auf PT_ERROR festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dc2a9-129">If one or more of the requested properties in the  _lpSPropTagArray_ parameter are not handled by the appropriate address book provider, their property types will be set to PT_ERROR.</span></span> <span data-ttu-id="dc2a9-130">Ihre Eigenschaftswerte werden auf MAPI_E_NOT_FOUND oder auf einen anderen Wert festgelegt, der einen spezifischeren Grund liefert, warum die Eigenschaften nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="dc2a9-130">Their property values will be set to either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason why the properties are not available.</span></span> <span data-ttu-id="dc2a9-131">Jede [SPropValue](spropvalue.md) -Struktur, die im _lpRecipList_ -Parameter enthalten ist, muss mithilfe der [MAPIAllocateBuffer](mapiallocatebuffer.md) -und [MAPIAllocateMore](mapiallocatemore.md) -Funktionen separat zugewiesen werden, damit Sie einzeln freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="dc2a9-131">Each [SPropValue](spropvalue.md) structure included in the  _lpRecipList_ parameter must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions so that it can be freed individually.</span></span> 
  
<span data-ttu-id="dc2a9-132">Weitere Informationen zu PT_ERROR finden Sie unter [Property Types](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="dc2a9-132">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dc2a9-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc2a9-133">See also</span></span>



[<span data-ttu-id="dc2a9-134">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="dc2a9-134">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="dc2a9-135">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="dc2a9-135">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="dc2a9-136">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="dc2a9-136">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="dc2a9-137">Kanonische PidTagEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dc2a9-137">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="dc2a9-138">SPropValue</span><span class="sxs-lookup"><span data-stu-id="dc2a9-138">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="dc2a9-139">SRowSet</span><span class="sxs-lookup"><span data-stu-id="dc2a9-139">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="dc2a9-140">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dc2a9-140">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

