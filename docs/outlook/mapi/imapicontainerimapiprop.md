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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8be3b1857d539f81e42d2ac3e5813afa73513a16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286720"
---
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="0c638-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0c638-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="0c638-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c638-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c638-105">Verwaltet Vorgänge auf hoher Ebene für Containerobjekte wie Adressbücher, Verteilerlisten und Ordner.</span><span class="sxs-lookup"><span data-stu-id="0c638-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="0c638-106">Die [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)und [IDistList: IMAPIContainer](idistlistimapicontainer.md) -Schnittstellen werden von **IMAPIContainer**abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0c638-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c638-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0c638-107">Header file:</span></span>  <br/> |<span data-ttu-id="0c638-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0c638-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0c638-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="0c638-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="0c638-110">Ordner-, Adressbuchcontainer-und Verteilerlistenobjekte</span><span class="sxs-lookup"><span data-stu-id="0c638-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="0c638-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0c638-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="0c638-112">Nachrichtenspeicher, Adressbuch und Remote Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="0c638-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="0c638-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0c638-113">Called by:</span></span>  <br/> |<span data-ttu-id="0c638-114">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="0c638-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="0c638-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="0c638-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0c638-116">IID_IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="0c638-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="0c638-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="0c638-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="0c638-118">LPMAPICONTAINER</span><span class="sxs-lookup"><span data-stu-id="0c638-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="0c638-119">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="0c638-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="0c638-120">Abstrakte Klasse, nie implementiert</span><span class="sxs-lookup"><span data-stu-id="0c638-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0c638-121">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="0c638-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0c638-122">GetContentable</span><span class="sxs-lookup"><span data-stu-id="0c638-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="0c638-123">Gibt einen Zeiger auf die Inhaltstabelle des Containers zurück.</span><span class="sxs-lookup"><span data-stu-id="0c638-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="0c638-124">GetHierarchy-Struktur</span><span class="sxs-lookup"><span data-stu-id="0c638-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="0c638-125">Gibt einen Zeiger auf die Hierarchietabelle des Containers zurück.</span><span class="sxs-lookup"><span data-stu-id="0c638-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="0c638-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="0c638-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="0c638-127">Öffnet ein Objekt im Container und gibt einen Schnittstellenzeiger für den weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="0c638-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="0c638-128">SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="0c638-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="0c638-129">Legt Suchkriterien für den Container fest.</span><span class="sxs-lookup"><span data-stu-id="0c638-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="0c638-130">GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="0c638-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="0c638-131">Ruft die Suchkriterien für den Container ab.</span><span class="sxs-lookup"><span data-stu-id="0c638-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="0c638-132">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="0c638-132">**Required properties**</span></span>|<span data-ttu-id="0c638-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="0c638-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0c638-134">**PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0c638-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0c638-135">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c638-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="0c638-136">**PR_CONTAINER_CONTENTS** ([Pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0c638-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0c638-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c638-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="0c638-138">**PR_CONTAINER_FLAGS** ([Pidtagcontainerflags (](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0c638-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0c638-139">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0c638-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c638-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c638-140">See also</span></span>



[<span data-ttu-id="0c638-141">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0c638-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

