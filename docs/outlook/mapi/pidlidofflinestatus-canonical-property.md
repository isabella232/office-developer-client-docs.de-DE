---
title: PidLidOfflineStatus (kanonische Eigenschaft)
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
ms.openlocfilehash: 34f50766c2c45d85bbb0bd9e12d32c5dd87e3cac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793684"
---
# <a name="pidlidofflinestatus-canonical-property"></a><span data-ttu-id="a503a-103">PidLidOfflineStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a503a-103">PidLidOfflineStatus Canonical Property</span></span>

  
  
<span data-ttu-id="a503a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a503a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a503a-105">Bestimmt den Status einer Dokumentdatei auf einem Server, der [MS-LISTSWS] implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="a503a-105">Determines the state of a document file on a server that implements [MS-LISTSWS].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a503a-106">Zugeordnete Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a503a-106">Associated properties</span></span>  <br/> |<span data-ttu-id="a503a-107">dispidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="a503a-107">dispidOfflineStatus</span></span>  <br/> |
|<span data-ttu-id="a503a-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="a503a-108">Property set:</span></span>  <br/> |<span data-ttu-id="a503a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a503a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a503a-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="a503a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a503a-111">0x000085B9</span><span class="sxs-lookup"><span data-stu-id="a503a-111">0x000085B9</span></span>  <br/> |
|<span data-ttu-id="a503a-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a503a-112">Data type:</span></span>  <br/> |<span data-ttu-id="a503a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a503a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a503a-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a503a-114">Area:</span></span>  <br/> |<span data-ttu-id="a503a-115">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="a503a-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a503a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a503a-116">Remarks</span></span>

<span data-ttu-id="a503a-117">In der folgenden Tabelle sind die möglichen Werte dieser Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a503a-117">The following table shows the possible values of this property.</span></span>
  
|<span data-ttu-id="a503a-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a503a-118">**Value**</span></span>|<span data-ttu-id="a503a-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a503a-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a503a-120">0</span><span class="sxs-lookup"><span data-stu-id="a503a-120">0</span></span>  <br/> |<span data-ttu-id="a503a-121">Dokument ist nicht ausgecheckt.</span><span class="sxs-lookup"><span data-stu-id="a503a-121">Document is not checked out.</span></span>  <br/> |
|<span data-ttu-id="a503a-122">1</span><span class="sxs-lookup"><span data-stu-id="a503a-122">1</span></span>  <br/> |<span data-ttu-id="a503a-123">Dokument wird für den aktuellen Benutzer ausgecheckt.</span><span class="sxs-lookup"><span data-stu-id="a503a-123">Document is checked out to the current user.</span></span>  <br/> |
|<span data-ttu-id="a503a-124">2</span><span class="sxs-lookup"><span data-stu-id="a503a-124">2</span></span>  <br/> |<span data-ttu-id="a503a-125">Dokument ist nicht ausgecheckt, aber der aktuelle Benutzer verfügt über eine Kopie der Datei zur Bearbeitung auf dem aktuellen Computer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a503a-125">Document is not checked out, but the current user has a copy of the file saved for editing on the current computer.</span></span>  <br/> |
   
<span data-ttu-id="a503a-126">Diese Eigenschaft wird lokal berechnet und wird nicht gesendet auf einen Server können Sie jederzeit, wenn ein Benutzer das Element an ein anderes Konto zieht.</span><span class="sxs-lookup"><span data-stu-id="a503a-126">This property is calculated locally and is not sent to a server at any time unless a user drags the item to another account.</span></span> <span data-ttu-id="a503a-127">In diesem Fall wird es als benutzerdefinierte Eigenschaft benutzerdefinierte behandelt.</span><span class="sxs-lookup"><span data-stu-id="a503a-127">In that case, it is treated as a user-defined custom property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a503a-128">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a503a-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a503a-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a503a-129">Protocol specifications</span></span>

<span data-ttu-id="a503a-130">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="a503a-130">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="a503a-131">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a503a-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a503a-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a503a-132">Header files</span></span>

<span data-ttu-id="a503a-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a503a-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="a503a-134">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a503a-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a503a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a503a-135">See also</span></span>



[<span data-ttu-id="a503a-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a503a-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a503a-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a503a-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a503a-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a503a-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a503a-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a503a-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

