---
title: IMAPIContainer IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer
api_type:
- COM
ms.assetid: d83fdd83-3e86-43c8-a73f-8e9e01b53371
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 38094895fed03884b138b02d4aa1ed87bcc6ea9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575700"
---
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="15989-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="15989-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="15989-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15989-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15989-105">Allgemeine Vorgänge auf Containerobjekten wie Adressbücher, Verteilerlisten und Ordner verwaltet.</span><span class="sxs-lookup"><span data-stu-id="15989-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="15989-106">Die [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md), und [IDistList: IMAPIContainer](idistlistimapicontainer.md) Schnittstellen **IMAPIContainer**abgeleitet sind.</span><span class="sxs-lookup"><span data-stu-id="15989-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15989-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="15989-107">Header file:</span></span>  <br/> |<span data-ttu-id="15989-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15989-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="15989-109">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="15989-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="15989-110">Ordner, Adressbuchcontainer und Verteilung List-Objekten</span><span class="sxs-lookup"><span data-stu-id="15989-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="15989-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="15989-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="15989-112">Nachrichtenspeicher, Adressbuch und remote-Transport-Anbieter</span><span class="sxs-lookup"><span data-stu-id="15989-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="15989-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="15989-113">Called by:</span></span>  <br/> |<span data-ttu-id="15989-114">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="15989-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="15989-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="15989-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="15989-116">IID_IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="15989-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="15989-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="15989-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="15989-118">LPMAPICONTAINER</span><span class="sxs-lookup"><span data-stu-id="15989-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="15989-119">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="15989-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="15989-120">Abstrakte Basisklasse, die nie implementiert</span><span class="sxs-lookup"><span data-stu-id="15989-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="15989-121">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="15989-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="15989-122">GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="15989-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="15989-123">Gibt einen Zeiger auf den Container Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="15989-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="15989-124">GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="15989-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="15989-125">Gibt einen Zeiger auf den Container Hierarchietabelle.</span><span class="sxs-lookup"><span data-stu-id="15989-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="15989-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="15989-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="15989-127">Öffnet ein Objekt im Container einen Schnittstellenzeiger für den weiteren Zugriff zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="15989-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="15989-128">SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="15989-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="15989-129">Stellt die Suchkriterien für den Container her.</span><span class="sxs-lookup"><span data-stu-id="15989-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="15989-130">GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="15989-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="15989-131">Ruft die Suchkriterien für den Container an.</span><span class="sxs-lookup"><span data-stu-id="15989-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="15989-132">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="15989-132">**Required properties**</span></span>|<span data-ttu-id="15989-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="15989-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="15989-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="15989-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="15989-135">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="15989-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="15989-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="15989-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="15989-137">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="15989-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="15989-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="15989-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="15989-139">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="15989-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="15989-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15989-140">See also</span></span>



[<span data-ttu-id="15989-141">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="15989-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

