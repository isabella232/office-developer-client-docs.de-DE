---
title: Kanonische Pidtagselectable (-Eigenschaft
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
ms.openlocfilehash: 17343a721cbcc642c8cffe95112f25710c0c130c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359017"
---
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="d6ba9-103">Kanonische Pidtagselectable (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d6ba9-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="d6ba9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6ba9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6ba9-105">Enthält TRUE, wenn der Eintrag in der einmaligen Tabelle ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d6ba9-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6ba9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d6ba9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6ba9-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="d6ba9-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="d6ba9-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d6ba9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d6ba9-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="d6ba9-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="d6ba9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d6ba9-110">Data type:</span></span>  <br/> |<span data-ttu-id="d6ba9-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d6ba9-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d6ba9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d6ba9-112">Area:</span></span>  <br/> |<span data-ttu-id="d6ba9-113">Adressbuchcontainer</span><span class="sxs-lookup"><span data-stu-id="d6ba9-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6ba9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6ba9-114">Remarks</span></span>

<span data-ttu-id="d6ba9-115">Diese Eigenschaft wird hauptsächlich zur visuellen Formatierung einer einmaligen Tabelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6ba9-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="d6ba9-116">Vorlagen können gruppiert werden, indem ein Eintrag erstellt wird, der die Überschrift für die Gruppe angibt.</span><span class="sxs-lookup"><span data-stu-id="d6ba9-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="d6ba9-117">Wenn Sie diese Eigenschaft für die Überschrift auf FALSE festlegen, wird sichergestellt, dass der Benutzer nur die tatsächlichen Vorlagen in der Gruppe und nicht diesen Überschriften Eintrag auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="d6ba9-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="d6ba9-118">Diese Eigenschaft gilt nur für eine einmalige Tabelle, nicht für eine Adressbuch-Hierarchietabelle.</span><span class="sxs-lookup"><span data-stu-id="d6ba9-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="d6ba9-119">MAPI ermöglicht es einem Adressbuchanbieter, Elemente visuell auf zweierlei Weise zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="d6ba9-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="d6ba9-120">Erstens können bestimmte Zeilen als Überschriften funktionieren, indem Sie nicht ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="d6ba9-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="d6ba9-121">Zweitens können die auswählbaren Elemente relativ zu ihren Überschriften eingerückt werden, indem Sie die **PR_DEPTH** ([pidtagdepth (](pidtagdepth-canonical-property.md))-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="d6ba9-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="d6ba9-122">Diese Eigenschaft wird in einer solchen Gruppierung verwendet, um anzugeben, ob dieses Element aus einer Liste ausgewählt werden kann, um eine einmalige Adresse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d6ba9-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="d6ba9-123">Wenn beispielsweise ein Client über mehrere Vorlagen zum Erstellen von Fax-Adressen verfügt, können diese wie folgt angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="d6ba9-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="d6ba9-124">FAX-Vorlagen (Tiefe 0, nicht auswählbar)</span><span class="sxs-lookup"><span data-stu-id="d6ba9-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="d6ba9-125">Local (Tiefe 1, auswählbar)</span><span class="sxs-lookup"><span data-stu-id="d6ba9-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="d6ba9-126">Long-Distance (Tiefe 1, auswählbar)</span><span class="sxs-lookup"><span data-stu-id="d6ba9-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d6ba9-127">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d6ba9-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d6ba9-128">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d6ba9-128">Protocol specifications</span></span>

<span data-ttu-id="d6ba9-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6ba9-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6ba9-130">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d6ba9-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d6ba9-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6ba9-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6ba9-132">Gibt die Eigenschaften und Vorgänge an, die für Adressbuchvorlagen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="d6ba9-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d6ba9-133">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="d6ba9-133">Header files</span></span>

<span data-ttu-id="d6ba9-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d6ba9-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6ba9-135">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="d6ba9-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="d6ba9-136">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="d6ba9-136">Mapitags.h</span></span>
  
> <span data-ttu-id="d6ba9-137">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="d6ba9-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6ba9-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6ba9-138">See also</span></span>



[<span data-ttu-id="d6ba9-139">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="d6ba9-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="d6ba9-140">Kanonische Pidtagfoldertype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d6ba9-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="d6ba9-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d6ba9-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6ba9-142">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d6ba9-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6ba9-143">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d6ba9-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6ba9-144">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d6ba9-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

