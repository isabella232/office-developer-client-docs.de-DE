---
title: Kanonische PidTagSelectable-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSelectable
api_type:
- COM
ms.assetid: eeecd957-dd50-4849-9698-8bc7106301e9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 225c435107ba79183c737ddb8e09cda1ffbd83f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795119"
---
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="ad95e-103">Kanonische PidTagSelectable-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ad95e-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="ad95e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad95e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad95e-105">Enthält True, wenn der Eintrag in der einmaligen Tabelle ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ad95e-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad95e-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ad95e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ad95e-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="ad95e-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="ad95e-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="ad95e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ad95e-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="ad95e-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="ad95e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ad95e-110">Data type:</span></span>  <br/> |<span data-ttu-id="ad95e-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ad95e-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ad95e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ad95e-112">Area:</span></span>  <br/> |<span data-ttu-id="ad95e-113">Adressbuchcontainer</span><span class="sxs-lookup"><span data-stu-id="ad95e-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad95e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ad95e-114">Remarks</span></span>

<span data-ttu-id="ad95e-115">Diese Eigenschaft wird in erster Linie für die visuelle Formatierung einer einmaligen Tabelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad95e-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="ad95e-116">Vorlagen können, indem Sie einen Eintrag, der angibt, die Überschrift für die Gruppe erstellen gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="ad95e-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="ad95e-117">Durch Festlegen dieser Eigenschaft auf false festgelegt, für die Überschrift wird sichergestellt, dass der Benutzer nur die eigentlichen Vorlagen in der Gruppe und nicht bei diesem Eintrag Überschrift auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="ad95e-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="ad95e-118">Diese Eigenschaft gilt nur für einer einmaligen Tabelle, nicht zu einer Address Book Hierarchie-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ad95e-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="ad95e-119">MAPI ermöglicht eine Adressbuchanbieter zum Gruppieren von Elementen visuell durch zweierlei.</span><span class="sxs-lookup"><span data-stu-id="ad95e-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="ad95e-120">Erstens können bestimmte Zeilen als Überschriften fungieren, werden Sie nicht ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="ad95e-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="ad95e-121">Zweitens können die auswählbaren Elemente relativ zu ihrer Überschriften mithilfe der **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))-Eigenschaft eingezogen werden.</span><span class="sxs-lookup"><span data-stu-id="ad95e-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="ad95e-122">Diese Eigenschaft wird in solchen Gruppierung verwendet, um anzugeben, ob dieses Element aus einer Liste zum Erstellen eines einmaligen ausgewählt werden kann oder nicht.</span><span class="sxs-lookup"><span data-stu-id="ad95e-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="ad95e-123">Beispielsweise wenn ein Client mehrere Vorlagen zum Erstellen von Faxadressen verfügt, können sie wie folgt angezeigt:</span><span class="sxs-lookup"><span data-stu-id="ad95e-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="ad95e-124">FAX-Vorlagen (Tiefe 0, nicht ausgewählt werden kann)</span><span class="sxs-lookup"><span data-stu-id="ad95e-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="ad95e-125">Lokale (Tiefe 1, auswählbar)</span><span class="sxs-lookup"><span data-stu-id="ad95e-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="ad95e-126">Ferngespräche (Tiefe 1, auswählbar)</span><span class="sxs-lookup"><span data-stu-id="ad95e-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ad95e-127">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ad95e-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ad95e-128">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ad95e-128">Protocol specifications</span></span>

<span data-ttu-id="ad95e-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad95e-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad95e-130">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ad95e-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ad95e-131">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad95e-131">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad95e-132">Gibt die Eigenschaften und Operationen, die für Address Book Vorlagen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ad95e-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ad95e-133">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ad95e-133">Header files</span></span>

<span data-ttu-id="ad95e-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ad95e-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="ad95e-135">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ad95e-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="ad95e-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ad95e-136">Mapitags.h</span></span>
  
> <span data-ttu-id="ad95e-137">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ad95e-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad95e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad95e-138">See also</span></span>



[<span data-ttu-id="ad95e-139">GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="ad95e-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="ad95e-140">Kanonische PidTagFolderType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ad95e-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="ad95e-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad95e-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ad95e-142">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad95e-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ad95e-143">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ad95e-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ad95e-144">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ad95e-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

