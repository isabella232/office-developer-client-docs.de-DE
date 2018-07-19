---
title: PidTagRowid (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowid
api_type:
- COM
ms.assetid: 0fdcb55a-2971-4c7d-b61e-7ada2d19d0e6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e8d0e79e01040c1cc3d46e73a7e6a456a915a67f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794986"
---
# <a name="pidtagrowid-canonical-property"></a><span data-ttu-id="5e31c-103">PidTagRowid (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5e31c-103">PidTagRowid Canonical Property</span></span>

  
  
<span data-ttu-id="5e31c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5e31c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5e31c-105">Enthält einen eindeutigen Bezeichner für einen Empfänger in einer Tabelle Empfänger oder Status.</span><span class="sxs-lookup"><span data-stu-id="5e31c-105">Contains a unique identifier for a recipient in a recipient table or status table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e31c-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5e31c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e31c-107">PR_ROWID</span><span class="sxs-lookup"><span data-stu-id="5e31c-107">PR_ROWID</span></span>  <br/> |
|<span data-ttu-id="5e31c-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="5e31c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5e31c-109">0 x 3000</span><span class="sxs-lookup"><span data-stu-id="5e31c-109">0x3000</span></span>  <br/> |
|<span data-ttu-id="5e31c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5e31c-110">Data type:</span></span>  <br/> |<span data-ttu-id="5e31c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5e31c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5e31c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5e31c-112">Area:</span></span>  <br/> |<span data-ttu-id="5e31c-113">Allgemeine MAPI</span><span class="sxs-lookup"><span data-stu-id="5e31c-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e31c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e31c-114">Remarks</span></span>

<span data-ttu-id="5e31c-115">Diese Eigenschaft ist ein temporären Wert, der nur für die Lebensdauer des Objekts gültig ist, die Besitzer der Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="5e31c-115">This property is a temporary value that is valid only for the life of the object that owns the table.</span></span> <span data-ttu-id="5e31c-116">Als Spalte der Tabelle angezeigt wird, aber nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5e31c-116">It appears as a column of the table but is not stored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5e31c-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5e31c-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5e31c-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5e31c-118">Protocol specifications</span></span>

<span data-ttu-id="5e31c-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e31c-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e31c-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5e31c-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5e31c-121">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e31c-121">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e31c-122">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="5e31c-122">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5e31c-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5e31c-123">Header files</span></span>

<span data-ttu-id="5e31c-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e31c-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e31c-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5e31c-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="5e31c-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5e31c-126">Mapitags.h</span></span>
  
> <span data-ttu-id="5e31c-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5e31c-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e31c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e31c-128">See also</span></span>



[<span data-ttu-id="5e31c-129">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="5e31c-129">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="5e31c-130">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="5e31c-130">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)


[<span data-ttu-id="5e31c-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e31c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e31c-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e31c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e31c-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5e31c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e31c-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5e31c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

