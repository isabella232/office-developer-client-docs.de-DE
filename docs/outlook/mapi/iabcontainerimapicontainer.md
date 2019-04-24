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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0905fbe2ba584aef49c50152aaf448267d477c10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348958"
---
# <a name="iabcontainer--imapicontainer"></a><span data-ttu-id="5b3c1-103">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="5b3c1-103">IABContainer : IMAPIContainer</span></span>

<span data-ttu-id="5b3c1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b3c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b3c1-105">Ermöglicht den Zugriff auf Adressbuchcontainer.</span><span class="sxs-lookup"><span data-stu-id="5b3c1-105">Provides access to address book containers.</span></span> <span data-ttu-id="5b3c1-106">MAPI-und Clientanwendungen rufen die Methoden von **IABContainer** auf, um die Namensauflösung auszuführen und Empfänger zu erstellen, zu kopieren und zu löschen.</span><span class="sxs-lookup"><span data-stu-id="5b3c1-106">MAPI and client applications call the methods of **IABContainer** to perform name resolution and to create, copy, and delete recipients.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5b3c1-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5b3c1-107">Header file:</span></span>  <br/> |<span data-ttu-id="5b3c1-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5b3c1-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5b3c1-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="5b3c1-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="5b3c1-110">Adressbuchcontainer-Objekte</span><span class="sxs-lookup"><span data-stu-id="5b3c1-110">Address book container objects</span></span>  <br/> |
|<span data-ttu-id="5b3c1-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="5b3c1-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="5b3c1-112">Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="5b3c1-112">Address book providers</span></span>  <br/> |
|<span data-ttu-id="5b3c1-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="5b3c1-113">Called by:</span></span>  <br/> |<span data-ttu-id="5b3c1-114">MAPI-und Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="5b3c1-114">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="5b3c1-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="5b3c1-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5b3c1-116">IID_IABContainer</span><span class="sxs-lookup"><span data-stu-id="5b3c1-116">IID_IABContainer</span></span>  <br/> |
|<span data-ttu-id="5b3c1-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="5b3c1-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="5b3c1-118">LPABCONT</span><span class="sxs-lookup"><span data-stu-id="5b3c1-118">LPABCONT</span></span>  <br/> |
|<span data-ttu-id="5b3c1-119">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="5b3c1-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="5b3c1-120">Durchgeführt</span><span class="sxs-lookup"><span data-stu-id="5b3c1-120">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5b3c1-121">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="5b3c1-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5b3c1-122">CreateEntry</span><span class="sxs-lookup"><span data-stu-id="5b3c1-122">CreateEntry</span></span>](iabcontainer-createentry.md) <br/> |<span data-ttu-id="5b3c1-123">Erstellt einen neuen Eintrag, bei dem es sich um einen Messagingbenutzer, eine Verteilerliste oder einen anderen Container handeln kann.</span><span class="sxs-lookup"><span data-stu-id="5b3c1-123">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>  <br/> |
|[<span data-ttu-id="5b3c1-124">CopyEntries</span><span class="sxs-lookup"><span data-stu-id="5b3c1-124">CopyEntries</span></span>](iabcontainer-copyentries.md) <br/> |<span data-ttu-id="5b3c1-125">Kopiert einen oder mehrere Einträge, in der Regel Messagingbenutzer oder Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="5b3c1-125">Copies one or more entries, typically messaging users or distribution lists.</span></span>  <br/> |
|[<span data-ttu-id="5b3c1-126">DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="5b3c1-126">DeleteEntries</span></span>](iabcontainer-deleteentries.md) <br/> |<span data-ttu-id="5b3c1-127">Entfernt einen oder mehrere Einträge, in der Regel Messagingbenutzer, Verteilerlisten oder andere Container.</span><span class="sxs-lookup"><span data-stu-id="5b3c1-127">Removes one or more entries, typically messaging users, distribution lists, or other containers.</span></span>  <br/> |
|[<span data-ttu-id="5b3c1-128">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="5b3c1-128">ResolveNames</span></span>](iabcontainer-resolvenames.md) <br/> |<span data-ttu-id="5b3c1-129">Führt die Namensauflösung für einen oder mehrere Empfänger Einträge aus.</span><span class="sxs-lookup"><span data-stu-id="5b3c1-129">Performs name resolution for one or more recipient entries.</span></span>  <br/> |
   
|<span data-ttu-id="5b3c1-130">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="5b3c1-130">**Required properties**</span></span>|<span data-ttu-id="5b3c1-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="5b3c1-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5b3c1-132">**PR_CONTAINER_FLAGS** ([Pidtagcontainerflags (](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b3c1-132">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5b3c1-133">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5b3c1-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="5b3c1-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b3c1-134">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5b3c1-135">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5b3c1-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="5b3c1-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b3c1-136">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5b3c1-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b3c1-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="5b3c1-138">**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b3c1-138">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5b3c1-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b3c1-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="5b3c1-140">**PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b3c1-140">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5b3c1-141">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b3c1-141">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="5b3c1-142">**Optionale Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="5b3c1-142">**Optional properties**</span></span>|<span data-ttu-id="5b3c1-143">**Access**</span><span class="sxs-lookup"><span data-stu-id="5b3c1-143">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5b3c1-144">**PR_CONTAINER_CONTENTS** ([Pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b3c1-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5b3c1-145">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b3c1-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="5b3c1-146">**PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b3c1-146">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5b3c1-147">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b3c1-147">Read-only</span></span>  <br/> |
|<span data-ttu-id="5b3c1-148">**PR_DEF_CREATE_DL** ([Pidtagdefcreatedl (](pidtagdefcreatedl-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b3c1-148">**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5b3c1-149">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b3c1-149">Read-only</span></span>  <br/> |
|<span data-ttu-id="5b3c1-150">**PR_DEF_CREATE_MAILUSER** ([Pidtagdefcreatemailuser (](pidtagdefcreatemailuser-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b3c1-150">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5b3c1-151">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b3c1-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="5b3c1-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b3c1-152">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5b3c1-153">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b3c1-153">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b3c1-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b3c1-154">Remarks</span></span>

<span data-ttu-id="5b3c1-155">Die **IABContainer** -Schnittstelle erbt indirekt von der [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) -Schnittstelle über die [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) und [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="5b3c1-155">The **IABContainer** interface inherits indirectly from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface through the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) and [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces.</span></span> <span data-ttu-id="5b3c1-156">Adressbuchanbieter implementieren die **IABContainer** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5b3c1-156">Address book providers implement the **IABContainer** interface.</span></span> 
  
<span data-ttu-id="5b3c1-157">Eine beliebige Anzahl von Messaging-Benutzerobjekten, Verteilerlisten und anderen Adressbuch Containern kann in einem Adressbuchcontainer vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="5b3c1-157">Any number of messaging user objects, distribution lists, and other address book containers can exist in an address book container.</span></span> <span data-ttu-id="5b3c1-158">Wie bei jedem Container können Clients oder Dienstanbieter einen Adressbuchcontainer verwenden, um einen seiner Einträge zu öffnen oder um eine Hierarchietabelle oder eine Inhaltstabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5b3c1-158">As with any container, clients or service providers can use an address book container to open one of its entries or to retrieve a hierarchy table or contents table.</span></span> <span data-ttu-id="5b3c1-159">Adressbuchcontainer bieten außerdem eine Namensauflösung und je nach Anbieter die Möglichkeit, Einträge hinzuzufügen, zu entfernen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5b3c1-159">Address book containers also provide name resolution and, depending on the provider, the ability to add, remove, or modify entries.</span></span>
  
<span data-ttu-id="5b3c1-160">MAPI definiert einen speziellen Adressbuchcontainer, der als persönliches Adressbuch (PAB) bezeichnet wird und Einträge aus anderen Containern enthält.</span><span class="sxs-lookup"><span data-stu-id="5b3c1-160">MAPI defines a special address book container called the personal address book (PAB) that holds entries copied from other containers.</span></span> <span data-ttu-id="5b3c1-161">Ein PAB kann immer geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5b3c1-161">A PAB is always modifiable.</span></span> <span data-ttu-id="5b3c1-162">Benutzer füllen Ihr PAB in der Regel mit Einträgen, die die Empfänger angeben, mit denen Sie am häufigsten kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="5b3c1-162">Users typically populate their PAB with entries designating the recipients with which they most frequently communicate.</span></span> <span data-ttu-id="5b3c1-163">Ein PAB kann auch einmalige Adressen und neue Empfänger enthalten, die noch nicht Bestandteileines Adressbuch Containers sind.</span><span class="sxs-lookup"><span data-stu-id="5b3c1-163">A PAB can also hold one-off addresses and new recipients not yet a part of any address book container.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5b3c1-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b3c1-164">See also</span></span>

- [<span data-ttu-id="5b3c1-165">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5b3c1-165">MAPI Interfaces</span></span>](mapi-interfaces.md)

