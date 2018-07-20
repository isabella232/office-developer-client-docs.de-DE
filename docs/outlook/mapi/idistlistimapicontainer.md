---
title: IDistList IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IDistList
api_type:
- COM
ms.assetid: bd8e1ddb-3027-428b-8964-81614f80282d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7fee3c84d6a4d4a94397f5197f45637b0c7dd2be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792056"
---
# <a name="idistlist--imapicontainer"></a><span data-ttu-id="74f4e-103">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="74f4e-103">IDistList : IMAPIContainer</span></span>

  
  
<span data-ttu-id="74f4e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="74f4e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="74f4e-105">Ermöglicht den Zugriff auf Verteilerlisten änderbare Adresse Adressbuch-Container.</span><span class="sxs-lookup"><span data-stu-id="74f4e-105">Provides access to distribution lists in modifiable address book containers.</span></span> <span data-ttu-id="74f4e-106">**IDistList** können erstellen, kopieren und Löschen von Verteilerlisten, neben dem namensauflösung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74f4e-106">**IDistList** can create, copy, and delete distribution lists, in addition to performing name resolution.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="74f4e-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="74f4e-107">Header file:</span></span>  <br/> |<span data-ttu-id="74f4e-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74f4e-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="74f4e-109">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="74f4e-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="74f4e-110">Verteilung List-Objekten</span><span class="sxs-lookup"><span data-stu-id="74f4e-110">Distribution list objects</span></span>  <br/> |
|<span data-ttu-id="74f4e-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="74f4e-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="74f4e-112">Von adressbuchanbietern implementierte</span><span class="sxs-lookup"><span data-stu-id="74f4e-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="74f4e-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="74f4e-113">Called by:</span></span>  <br/> |<span data-ttu-id="74f4e-114">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="74f4e-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="74f4e-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="74f4e-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="74f4e-116">IID_IDistList</span><span class="sxs-lookup"><span data-stu-id="74f4e-116">IID_IDistList</span></span>  <br/> |
|<span data-ttu-id="74f4e-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="74f4e-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="74f4e-118">LPDISTLIST</span><span class="sxs-lookup"><span data-stu-id="74f4e-118">LPDISTLIST</span></span>  <br/> |
|<span data-ttu-id="74f4e-119">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="74f4e-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="74f4e-120">Durchgeführt</span><span class="sxs-lookup"><span data-stu-id="74f4e-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="74f4e-121">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="74f4e-121">Vtable order</span></span>

<span data-ttu-id="74f4e-122">Diese Schnittstelle hat keinen eindeutigen Methoden.</span><span class="sxs-lookup"><span data-stu-id="74f4e-122">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="74f4e-123">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="74f4e-123">**Required properties**</span></span>|<span data-ttu-id="74f4e-124">**Zugriff**</span><span class="sxs-lookup"><span data-stu-id="74f4e-124">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="74f4e-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="74f4e-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="74f4e-126">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="74f4e-126">Read/write</span></span>  <br/> |
|<span data-ttu-id="74f4e-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="74f4e-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="74f4e-128">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="74f4e-128">Read/write</span></span>  <br/> |
|<span data-ttu-id="74f4e-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="74f4e-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="74f4e-130">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="74f4e-130">Read-only</span></span>  <br/> |
|<span data-ttu-id="74f4e-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="74f4e-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="74f4e-132">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="74f4e-132">Read-only</span></span>  <br/> |
|<span data-ttu-id="74f4e-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="74f4e-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="74f4e-134">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="74f4e-134">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74f4e-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74f4e-135">Remarks</span></span>

<span data-ttu-id="74f4e-136">Die **IDistList** -Schnittstelle erbt von [IMAPIContainer](imapicontainerimapiprop.md) und enthält die gleichen Methoden als Address Book Container.</span><span class="sxs-lookup"><span data-stu-id="74f4e-136">The **IDistList** interface inherits from [IMAPIContainer](imapicontainerimapiprop.md) and includes the same methods as address book containers.</span></span> <span data-ttu-id="74f4e-137">Aus diesem Grund, da die Methoden der Schnittstelle **IDistList** identisch mit denen der [IABContainer](iabcontainerimapicontainer.md) Schnittstelle sind, sind sie nicht hier nicht dupliziert.</span><span class="sxs-lookup"><span data-stu-id="74f4e-137">Therefore, because the methods of the **IDistList** interface are identical to those of the [IABContainer](iabcontainerimapicontainer.md) interface, they are not duplicated here.</span></span> 
  
<span data-ttu-id="74f4e-138">Eine Verteilerliste oder ein Objekt, das **IDistList** implementiert ist eine Auflistung von messaging Benutzerobjekte oder einzelne Empfänger.</span><span class="sxs-lookup"><span data-stu-id="74f4e-138">A distribution list or object that implements **IDistList** is a collection of messaging user objects, or individual recipients.</span></span> <span data-ttu-id="74f4e-139">Eine Verteilerliste kann alle messaging Benutzerobjekte oder einige messaging-Benutzer und einige Verteilerlisten bestehen.</span><span class="sxs-lookup"><span data-stu-id="74f4e-139">A distribution list can consist of all messaging user objects, or some messaging user and some distribution lists.</span></span> 
  
<span data-ttu-id="74f4e-140">Es sind in der Regel zwei Arten von Verteilerlisten:</span><span class="sxs-lookup"><span data-stu-id="74f4e-140">There are typically two types of distribution lists:</span></span>
  
- <span data-ttu-id="74f4e-141">Verteilerlisten, die von der zugrunde liegenden messaging-System erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="74f4e-141">Distribution lists that are expanded by the underlying messaging system.</span></span> <span data-ttu-id="74f4e-142">Diese Art der Liste hat eine Adresse **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) und ist gleich behandelt, als ob es sich um einen einzelnen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="74f4e-142">This type of list has an address, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and is treated the same as if it were an individual recipient.</span></span> 
    
- <span data-ttu-id="74f4e-143">Verteilerlisten, die in einem lokalen Container vorhanden und werden von der Clientanwendung erweitert.</span><span class="sxs-lookup"><span data-stu-id="74f4e-143">Distribution lists that exist in a local container and are expanded by the client application.</span></span>
    
<span data-ttu-id="74f4e-144">Die folgenden: Eigenschaften von optional Verteilerlisten</span><span class="sxs-lookup"><span data-stu-id="74f4e-144">Optional distribution list properties include the following:</span></span>
  
- <span data-ttu-id="74f4e-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="74f4e-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="74f4e-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="74f4e-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="74f4e-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="74f4e-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span></span> 
    
<span data-ttu-id="74f4e-148">Beachten Sie, dass **PR_ADDRTYPE** erforderlich ist, aber **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) nicht.</span><span class="sxs-lookup"><span data-stu-id="74f4e-148">Notice that **PR_ADDRTYPE** is required, but **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is not.</span></span> <span data-ttu-id="74f4e-149">Dies liegt daran eine Verteilerliste, ohne eine e-Mail-Adresse kann weiterhin Nachrichten empfangen, aber die Mitgliederliste erweitert werden muss.</span><span class="sxs-lookup"><span data-stu-id="74f4e-149">That is because a distribution list without an email address can still receive messages, but its member list must be expanded.</span></span> <span data-ttu-id="74f4e-150">Wenn die **PR_ADDRTYPE** -Eigenschaft auf MAPIPDL festgelegt ist, führt MAPI die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="74f4e-150">If the **PR_ADDRTYPE** property is set to MAPIPDL, MAPI performs the expansion.</span></span> <span data-ttu-id="74f4e-151">Wenn **PR_ADDRTYPE** einen anderen Wert als MAPIPDL ist, führt der Adressbuchhierarchie die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="74f4e-151">If **PR_ADDRTYPE** is a value other than MAPIPDL, the transport provider performs the expansion.</span></span> 
  
<span data-ttu-id="74f4e-152">Weitere Informationen dazu, wie Sie die Referenz-Einträge für die parallelen Methoden des **IABContainer**finden Sie die **IDistList** -Methoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="74f4e-152">For additional information about how to use the **IDistList** methods, see the reference entries for the parallel methods of **IABContainer**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="74f4e-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74f4e-153">See also</span></span>



[<span data-ttu-id="74f4e-154">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="74f4e-154">MAPI Interfaces</span></span>](mapi-interfaces.md)

