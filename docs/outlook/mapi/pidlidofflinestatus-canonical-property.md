---
title: Kanonische Pidlidofflinestatus (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 537b45420390903d67722c074a1edcc04a0aede8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326299"
---
# <a name="pidlidofflinestatus-canonical-property"></a><span data-ttu-id="41771-103">Kanonische Pidlidofflinestatus (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="41771-103">PidLidOfflineStatus Canonical Property</span></span>

  
  
<span data-ttu-id="41771-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41771-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41771-105">Bestimmt den Status einer Dokumentdatei auf einem Server, der [MS-LISTSWS] implementiert.</span><span class="sxs-lookup"><span data-stu-id="41771-105">Determines the state of a document file on a server that implements [MS-LISTSWS].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="41771-106">Zugeordnete Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41771-106">Associated properties</span></span>  <br/> |<span data-ttu-id="41771-107">dispidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="41771-107">dispidOfflineStatus</span></span>  <br/> |
|<span data-ttu-id="41771-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="41771-108">Property set:</span></span>  <br/> |<span data-ttu-id="41771-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="41771-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="41771-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="41771-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="41771-111">0x000085B9</span><span class="sxs-lookup"><span data-stu-id="41771-111">0x000085B9</span></span>  <br/> |
|<span data-ttu-id="41771-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="41771-112">Data type:</span></span>  <br/> |<span data-ttu-id="41771-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="41771-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="41771-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="41771-114">Area:</span></span>  <br/> |<span data-ttu-id="41771-115">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="41771-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41771-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41771-116">Remarks</span></span>

<span data-ttu-id="41771-117">In der folgenden Tabelle sind die möglichen Werte dieser Eigenschaft aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="41771-117">The following table shows the possible values of this property.</span></span>
  
|<span data-ttu-id="41771-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="41771-118">**Value**</span></span>|<span data-ttu-id="41771-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="41771-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="41771-120">0</span><span class="sxs-lookup"><span data-stu-id="41771-120">0</span></span>  <br/> |<span data-ttu-id="41771-121">Dokument ist nicht ausgecheckt.</span><span class="sxs-lookup"><span data-stu-id="41771-121">Document is not checked out.</span></span>  <br/> |
|<span data-ttu-id="41771-122">1</span><span class="sxs-lookup"><span data-stu-id="41771-122">1</span></span>  <br/> |<span data-ttu-id="41771-123">Dokument ist für den aktuellen Benutzer ausgecheckt.</span><span class="sxs-lookup"><span data-stu-id="41771-123">Document is checked out to the current user.</span></span>  <br/> |
|<span data-ttu-id="41771-124">2</span><span class="sxs-lookup"><span data-stu-id="41771-124">2</span></span>  <br/> |<span data-ttu-id="41771-125">Dokument ist nicht ausgecheckt, aber der aktuelle Benutzer verfügt über eine Kopie der Datei, die zum Bearbeiten auf dem aktuellen Computer gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="41771-125">Document is not checked out, but the current user has a copy of the file saved for editing on the current computer.</span></span>  <br/> |
   
<span data-ttu-id="41771-126">Diese Eigenschaft wird lokal berechnet und wird nicht an einen Server gesendet, es sei denn, ein Benutzer zieht das Element in ein anderes Konto.</span><span class="sxs-lookup"><span data-stu-id="41771-126">This property is calculated locally and is not sent to a server at any time unless a user drags the item to another account.</span></span> <span data-ttu-id="41771-127">In diesem Fall wird es als benutzerdefinierte benutzerdefinierte Eigenschaft behandelt.</span><span class="sxs-lookup"><span data-stu-id="41771-127">In that case, it is treated as a user-defined custom property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="41771-128">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="41771-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="41771-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="41771-129">Protocol specifications</span></span>

<span data-ttu-id="41771-130">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="41771-130">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="41771-131">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="41771-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="41771-132">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="41771-132">Header files</span></span>

<span data-ttu-id="41771-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="41771-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="41771-134">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="41771-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41771-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41771-135">See also</span></span>



[<span data-ttu-id="41771-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41771-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="41771-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41771-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="41771-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="41771-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="41771-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="41771-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

