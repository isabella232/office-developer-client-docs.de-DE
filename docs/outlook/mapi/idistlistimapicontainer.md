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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 463d81a6692b6071cada0ad22e7343020563e41c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350890"
---
# <a name="idistlist--imapicontainer"></a><span data-ttu-id="63867-103">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="63867-103">IDistList : IMAPIContainer</span></span>

  
  
<span data-ttu-id="63867-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63867-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63867-105">Ermöglicht den Zugriff auf Verteilerlisten in änderbaren Adressbuch Containern.</span><span class="sxs-lookup"><span data-stu-id="63867-105">Provides access to distribution lists in modifiable address book containers.</span></span> <span data-ttu-id="63867-106">**IDistList** können neben der Namensauflösung auch Verteilerlisten erstellen, kopieren und löschen.</span><span class="sxs-lookup"><span data-stu-id="63867-106">**IDistList** can create, copy, and delete distribution lists, in addition to performing name resolution.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="63867-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="63867-107">Header file:</span></span>  <br/> |<span data-ttu-id="63867-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="63867-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="63867-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="63867-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="63867-110">Verteilerlistenobjekte</span><span class="sxs-lookup"><span data-stu-id="63867-110">Distribution list objects</span></span>  <br/> |
|<span data-ttu-id="63867-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="63867-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="63867-112">Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="63867-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="63867-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="63867-113">Called by:</span></span>  <br/> |<span data-ttu-id="63867-114">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="63867-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="63867-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="63867-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="63867-116">IID_IDistList</span><span class="sxs-lookup"><span data-stu-id="63867-116">IID_IDistList</span></span>  <br/> |
|<span data-ttu-id="63867-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="63867-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="63867-118">LPDISTLIST</span><span class="sxs-lookup"><span data-stu-id="63867-118">LPDISTLIST</span></span>  <br/> |
|<span data-ttu-id="63867-119">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="63867-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="63867-120">Durchgeführt</span><span class="sxs-lookup"><span data-stu-id="63867-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="63867-121">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="63867-121">Vtable order</span></span>

<span data-ttu-id="63867-122">Diese Schnittstelle hat keine eindeutigen Methoden.</span><span class="sxs-lookup"><span data-stu-id="63867-122">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="63867-123">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="63867-123">**Required properties**</span></span>|<span data-ttu-id="63867-124">**Access**</span><span class="sxs-lookup"><span data-stu-id="63867-124">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="63867-125">**PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="63867-125">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="63867-126">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="63867-126">Read/write</span></span>  <br/> |
|<span data-ttu-id="63867-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="63867-127">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="63867-128">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="63867-128">Read/write</span></span>  <br/> |
|<span data-ttu-id="63867-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="63867-129">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="63867-130">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63867-130">Read-only</span></span>  <br/> |
|<span data-ttu-id="63867-131">**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="63867-131">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="63867-132">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63867-132">Read-only</span></span>  <br/> |
|<span data-ttu-id="63867-133">**PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="63867-133">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="63867-134">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63867-134">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63867-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63867-135">Remarks</span></span>

<span data-ttu-id="63867-136">Die **IDistList** -Schnittstelle erbt von [IMAPIContainer](imapicontainerimapiprop.md) und enthält die gleichen Methoden wie Adressbuchcontainer.</span><span class="sxs-lookup"><span data-stu-id="63867-136">The **IDistList** interface inherits from [IMAPIContainer](imapicontainerimapiprop.md) and includes the same methods as address book containers.</span></span> <span data-ttu-id="63867-137">Da die Methoden der **IDistList** -Schnittstelle mit denen der [IABContainer](iabcontainerimapicontainer.md) -Schnittstelle identisch sind, werden Sie daher nicht dupliziert.</span><span class="sxs-lookup"><span data-stu-id="63867-137">Therefore, because the methods of the **IDistList** interface are identical to those of the [IABContainer](iabcontainerimapicontainer.md) interface, they are not duplicated here.</span></span> 
  
<span data-ttu-id="63867-138">Eine Verteilerliste oder ein Objekt, das **IDistList** implementiert, ist eine Sammlung von Messaging-Benutzerobjekten oder einzelnen Empfängern.</span><span class="sxs-lookup"><span data-stu-id="63867-138">A distribution list or object that implements **IDistList** is a collection of messaging user objects, or individual recipients.</span></span> <span data-ttu-id="63867-139">Eine Verteilerliste kann aus allen Messaging-Benutzerobjekten oder einigen Messaging Benutzern und einigen Verteilerlisten bestehen.</span><span class="sxs-lookup"><span data-stu-id="63867-139">A distribution list can consist of all messaging user objects, or some messaging user and some distribution lists.</span></span> 
  
<span data-ttu-id="63867-140">Es gibt in der Regel zwei Arten von Verteilerlisten:</span><span class="sxs-lookup"><span data-stu-id="63867-140">There are typically two types of distribution lists:</span></span>
  
- <span data-ttu-id="63867-141">Verteilerlisten, die durch das zugrunde liegende Messagingsystem erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="63867-141">Distribution lists that are expanded by the underlying messaging system.</span></span> <span data-ttu-id="63867-142">Dieser Listentyp hat eine Adresse, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) und wird genauso behandelt, als sei es ein einzelner Empfänger.</span><span class="sxs-lookup"><span data-stu-id="63867-142">This type of list has an address, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and is treated the same as if it were an individual recipient.</span></span> 
    
- <span data-ttu-id="63867-143">Verteilerlisten, die in einem lokalen Container vorhanden sind und von der Clientanwendung erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="63867-143">Distribution lists that exist in a local container and are expanded by the client application.</span></span>
    
<span data-ttu-id="63867-144">Optionale Verteilerlisteneigenschaften:</span><span class="sxs-lookup"><span data-stu-id="63867-144">Optional distribution list properties include the following:</span></span>
  
- <span data-ttu-id="63867-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="63867-145">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="63867-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="63867-146">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="63867-147">**PR_DETAILS_TABLE** ([Pidtagdetailstable (](pidtagdetailstable-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="63867-147">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))</span></span> 
    
<span data-ttu-id="63867-148">Beachten Sie, dass **PR_ADDRTYPE** erforderlich ist, aber **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) nicht.</span><span class="sxs-lookup"><span data-stu-id="63867-148">Notice that **PR_ADDRTYPE** is required, but **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is not.</span></span> <span data-ttu-id="63867-149">Das liegt daran, dass eine Verteilerliste ohne eine e-Mail-Adresse weiterhin Nachrichten empfangen kann, ihre Mitgliederliste jedoch erweitert werden muss.</span><span class="sxs-lookup"><span data-stu-id="63867-149">That is because a distribution list without an email address can still receive messages, but its member list must be expanded.</span></span> <span data-ttu-id="63867-150">Wenn die **PR_ADDRTYPE** -Eigenschaft auf MAPIPDL festgelegt ist, wird die Erweiterung von MAPI ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63867-150">If the **PR_ADDRTYPE** property is set to MAPIPDL, MAPI performs the expansion.</span></span> <span data-ttu-id="63867-151">Wenn **PR_ADDRTYPE** ein anderer Wert als MAPIPDL ist, führt der Transportanbieter die Erweiterung aus.</span><span class="sxs-lookup"><span data-stu-id="63867-151">If **PR_ADDRTYPE** is a value other than MAPIPDL, the transport provider performs the expansion.</span></span> 
  
<span data-ttu-id="63867-152">Weitere Informationen zur Verwendung der **IDistList** -Methoden finden Sie in den Referenz Einträgen für die parallelen Methoden von **IABContainer**.</span><span class="sxs-lookup"><span data-stu-id="63867-152">For additional information about how to use the **IDistList** methods, see the reference entries for the parallel methods of **IABContainer**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="63867-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63867-153">See also</span></span>



[<span data-ttu-id="63867-154">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="63867-154">MAPI Interfaces</span></span>](mapi-interfaces.md)

