---
title: IABContainer IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer
api_type:
- COM
ms.assetid: 1f5ce6e0-b79a-4da2-b014-8c00cd72912e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0905fbe2ba584aef49c50152aaf448267d477c10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348958"
---
# <a name="iabcontainer--imapicontainer"></a><span data-ttu-id="53909-103">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="53909-103">IABContainer : IMAPIContainer</span></span>

<span data-ttu-id="53909-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53909-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53909-105">Bietet Zugriff auf Adressbuchcontainer.</span><span class="sxs-lookup"><span data-stu-id="53909-105">Provides access to address book containers.</span></span> <span data-ttu-id="53909-106">MAPI- und Clientanwendungen rufen die Methoden von **IABContainer** auf, um Namensauflösungen durchzuführen und Empfänger zu erstellen, zu kopieren und zu löschen.</span><span class="sxs-lookup"><span data-stu-id="53909-106">MAPI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53909-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="53909-107">Header file:</span></span>  <br/> |<span data-ttu-id="53909-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53909-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="53909-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="53909-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="53909-110">Adressbuchcontainerobjekte</span><span class="sxs-lookup"><span data-stu-id="53909-110">Address book container objects</span></span>  <br/> |
|<span data-ttu-id="53909-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="53909-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="53909-112">Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="53909-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="53909-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="53909-113">Called by:</span></span>  <br/> |<span data-ttu-id="53909-114">MAPI- und Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="53909-114">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="53909-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="53909-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="53909-116">IID_IABContainer</span><span class="sxs-lookup"><span data-stu-id="53909-116">IID_IABContainer</span></span>  <br/> |
|<span data-ttu-id="53909-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="53909-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="53909-118">LPABCONT</span><span class="sxs-lookup"><span data-stu-id="53909-118">LPABCONT</span></span>  <br/> |
|<span data-ttu-id="53909-119">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="53909-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="53909-120">Transacted</span><span class="sxs-lookup"><span data-stu-id="53909-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="53909-121">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="53909-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="53909-122">CreateEntry</span><span class="sxs-lookup"><span data-stu-id="53909-122">CreateEntry</span></span>](iabcontainer-createentry.md) <br/> |<span data-ttu-id="53909-123">Erstellt einen neuen Eintrag, der ein Messagingbenutzer, eine Verteilerliste oder ein anderer Container sein kann.</span><span class="sxs-lookup"><span data-stu-id="53909-123">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>  <br/> |
|[<span data-ttu-id="53909-124">CopyEntries</span><span class="sxs-lookup"><span data-stu-id="53909-124">CopyEntries</span></span>](iabcontainer-copyentries.md) <br/> |<span data-ttu-id="53909-125">Kopiert einen oder mehrere Einträge, in der Regel Messagingbenutzer oder Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="53909-125">Copies one or more entries, typically messaging users or distribution lists.</span></span>  <br/> |
|[<span data-ttu-id="53909-126">DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="53909-126">DeleteEntries</span></span>](iabcontainer-deleteentries.md) <br/> |<span data-ttu-id="53909-127">Entfernt einen oder mehrere Einträge, in der Regel Messagingbenutzer, Verteilerlisten oder andere Container.</span><span class="sxs-lookup"><span data-stu-id="53909-127">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>  <br/> |
|[<span data-ttu-id="53909-128">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="53909-128">ResolveNames</span></span>](iabcontainer-resolvenames.md) <br/> |<span data-ttu-id="53909-129">Führt die Namensauflösung für einen oder mehrere Empfängereinträge aus.</span><span class="sxs-lookup"><span data-stu-id="53909-129">Performs name resolution for one or more recipient entries.</span></span>  <br/> |
   
|<span data-ttu-id="53909-130">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="53909-130">**Required properties**</span></span>|<span data-ttu-id="53909-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="53909-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53909-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53909-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53909-133">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="53909-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="53909-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53909-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53909-135">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="53909-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="53909-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53909-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53909-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53909-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="53909-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53909-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53909-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53909-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="53909-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53909-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53909-141">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53909-141">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="53909-142">**Optionale Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="53909-142">**Optional properties**</span></span>|<span data-ttu-id="53909-143">**Access**</span><span class="sxs-lookup"><span data-stu-id="53909-143">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53909-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53909-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53909-145">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53909-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="53909-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53909-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53909-147">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53909-147">Read-only</span></span>  <br/> |
|<span data-ttu-id="53909-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53909-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53909-149">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53909-149">Read-only</span></span>  <br/> |
|<span data-ttu-id="53909-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53909-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53909-151">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53909-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="53909-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53909-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53909-153">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53909-153">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53909-154">Hinweise</span><span class="sxs-lookup"><span data-stu-id="53909-154">Remarks</span></span>

<span data-ttu-id="53909-155">Die **IABContainer-Schnittstelle** erbt indirekt von der [IUnknown-Schnittstelle](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) über die [SCHNITTSTELLEN IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) und [IMAPIProp : IUnknown.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="53909-155">The **IABContainer** interface inherits indirectly from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface through the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) and [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces.</span></span> <span data-ttu-id="53909-156">Adressbuchanbieter implementieren die **IABContainer-Schnittstelle.**</span><span class="sxs-lookup"><span data-stu-id="53909-156">Address book providers implement the **IABContainer** interface.</span></span> 
  
<span data-ttu-id="53909-157">Eine beliebige Anzahl von Messagingbenutzerobjekten, Verteilerlisten und anderen Adressbuchcontainern kann in einem Adressbuchcontainer vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="53909-157">Any number of messaging user objects, distribution lists, and other address book containers can exist in an address book container.</span></span> <span data-ttu-id="53909-158">Wie bei jedem Container können Clients oder Dienstanbieter einen Adressbuchcontainer verwenden, um einen seiner Einträge zu öffnen oder eine Hierarchietabelle oder Inhaltstabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="53909-158">As with any container, clients or service providers can use an address book container to open one of its entries or to retrieve a hierarchy table or contents table.</span></span> <span data-ttu-id="53909-159">Adressbuchcontainer bieten auch die Namensauflösung und je nach Anbieter die Möglichkeit, Einträge hinzuzufügen, zu entfernen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="53909-159">Address book containers also provide name resolution and, depending on the provider, the ability to add, remove, or modify entries.</span></span>
  
<span data-ttu-id="53909-160">MAPI definiert einen speziellen Adressbuchcontainer namens Persönliches Adressbuch (PAB), der Einträge enthält, die aus anderen Containern kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="53909-160">MAPI defines a special address book container called the personal address book (PAB) that holds entries copied from other containers.</span></span> <span data-ttu-id="53909-161">Ein PAB ist immer veränderbar.</span><span class="sxs-lookup"><span data-stu-id="53909-161">A PAB is always modifiable.</span></span> <span data-ttu-id="53909-162">Benutzer füllen ihr PAB in der Regel mit Einträgen auf, mit denen die Empfänger bezeichnet werden, mit denen sie am häufigsten kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="53909-162">Users typically populate their PAB with entries designating the recipients with which they most frequently communicate.</span></span> <span data-ttu-id="53909-163">Ein PAB kann auch einmal adressen und neue Empfänger enthalten, die noch nicht Teil eines Adressbuchcontainers sind.</span><span class="sxs-lookup"><span data-stu-id="53909-163">A PAB can also hold one-off addresses and new recipients not yet a part of any address book container.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="53909-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53909-164">See also</span></span>

- [<span data-ttu-id="53909-165">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="53909-165">MAPI Interfaces</span></span>](mapi-interfaces.md)

