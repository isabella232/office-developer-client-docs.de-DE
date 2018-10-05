---
title: PidTagAccessLevel (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccessLevel
api_type:
- HeaderDef
ms.assetid: 8f7119c7-ffc3-47cf-aa1b-b4e56bcc5a24
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5138f5d255f6a90d2891fe2cf5ce92513463fa31
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389799"
---
# <a name="pidtagaccesslevel-canonical-property"></a><span data-ttu-id="fe2a9-103">PidTagAccessLevel (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fe2a9-103">PidTagAccessLevel Canonical Property</span></span>

  
  
<span data-ttu-id="fe2a9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe2a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe2a9-105">Gibt den Client Zugriffsebene auf das Objekt an.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-105">Indicates the client's access level to the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fe2a9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fe2a9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fe2a9-107">PR_ACCESS_LEVEL</span><span class="sxs-lookup"><span data-stu-id="fe2a9-107">PR_ACCESS_LEVEL</span></span>  <br/> |
|<span data-ttu-id="fe2a9-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="fe2a9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fe2a9-109">0x0FF7</span><span class="sxs-lookup"><span data-stu-id="fe2a9-109">0x0FF7</span></span>  <br/> |
|<span data-ttu-id="fe2a9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fe2a9-110">Data type:</span></span>  <br/> |<span data-ttu-id="fe2a9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fe2a9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fe2a9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fe2a9-112">Area:</span></span>  <br/> |<span data-ttu-id="fe2a9-113">Access-Steuerelementeigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe2a9-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe2a9-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fe2a9-114">Remarks</span></span>

<span data-ttu-id="fe2a9-115">Diese Eigenschaft ist schreibgeschützt für den Client.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-115">This property is read-only for the client.</span></span> <span data-ttu-id="fe2a9-116">Es muss eine der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="fe2a9-116">It must be one of the following values:</span></span>
  
|<span data-ttu-id="fe2a9-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fe2a9-117">**Value**</span></span>|<span data-ttu-id="fe2a9-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fe2a9-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe2a9-119">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe2a9-119">0x00000000</span></span>  <br/> |<span data-ttu-id="fe2a9-120">Read-Only</span><span class="sxs-lookup"><span data-stu-id="fe2a9-120">Read-Only</span></span>  <br/> |
|<span data-ttu-id="fe2a9-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fe2a9-121">0x00000001</span></span>  <br/> |<span data-ttu-id="fe2a9-122">Ändern</span><span class="sxs-lookup"><span data-stu-id="fe2a9-122">Modify</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="fe2a9-123">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fe2a9-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fe2a9-124">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="fe2a9-124">Protocol specifications</span></span>

<span data-ttu-id="fe2a9-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe2a9-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe2a9-126">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fe2a9-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe2a9-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe2a9-128">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fe2a9-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="fe2a9-129">Header files</span></span>

<span data-ttu-id="fe2a9-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe2a9-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="fe2a9-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="fe2a9-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fe2a9-132">Mapitags.h</span></span>
  
> <span data-ttu-id="fe2a9-133">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe2a9-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe2a9-134">See also</span></span>



[<span data-ttu-id="fe2a9-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe2a9-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fe2a9-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe2a9-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fe2a9-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fe2a9-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fe2a9-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fe2a9-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

