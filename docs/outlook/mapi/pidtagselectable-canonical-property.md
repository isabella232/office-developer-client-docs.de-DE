---
title: PidTagSelectable (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d376a5219125866f467be01709a6a611ed8d47f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576421"
---
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="a2c52-103">PidTagSelectable (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a2c52-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="a2c52-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2c52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2c52-105">Enthält True, wenn der Eintrag in der einmaligen Tabelle ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a2c52-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a2c52-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a2c52-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a2c52-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="a2c52-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="a2c52-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a2c52-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a2c52-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="a2c52-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="a2c52-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a2c52-110">Data type:</span></span>  <br/> |<span data-ttu-id="a2c52-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a2c52-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a2c52-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a2c52-112">Area:</span></span>  <br/> |<span data-ttu-id="a2c52-113">Adressbuchcontainer</span><span class="sxs-lookup"><span data-stu-id="a2c52-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2c52-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="a2c52-114">Remarks</span></span>

<span data-ttu-id="a2c52-115">Diese Eigenschaft wird in erster Linie für die visuelle Formatierung einer einmaligen Tabelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="a2c52-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="a2c52-116">Vorlagen können, indem Sie einen Eintrag, der angibt, die Überschrift für die Gruppe erstellen gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="a2c52-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="a2c52-117">Durch Festlegen dieser Eigenschaft auf false festgelegt, für die Überschrift wird sichergestellt, dass der Benutzer nur die eigentlichen Vorlagen in der Gruppe und nicht bei diesem Eintrag Überschrift auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="a2c52-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="a2c52-118">Diese Eigenschaft gilt nur für einer einmaligen Tabelle, nicht zu einer Address Book Hierarchie-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a2c52-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="a2c52-119">MAPI ermöglicht eine Adressbuchanbieter zum Gruppieren von Elementen visuell durch zweierlei.</span><span class="sxs-lookup"><span data-stu-id="a2c52-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="a2c52-120">Erstens können bestimmte Zeilen als Überschriften fungieren, werden Sie nicht ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="a2c52-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="a2c52-121">Zweitens können die auswählbaren Elemente relativ zu ihrer Überschriften mithilfe der **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))-Eigenschaft eingezogen werden.</span><span class="sxs-lookup"><span data-stu-id="a2c52-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="a2c52-122">Diese Eigenschaft wird in solchen Gruppierung verwendet, um anzugeben, ob dieses Element aus einer Liste zum Erstellen eines einmaligen ausgewählt werden kann oder nicht.</span><span class="sxs-lookup"><span data-stu-id="a2c52-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="a2c52-123">Beispielsweise wenn ein Client mehrere Vorlagen zum Erstellen von Faxadressen verfügt, können sie wie folgt angezeigt:</span><span class="sxs-lookup"><span data-stu-id="a2c52-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="a2c52-124">FAX-Vorlagen (Tiefe 0, nicht ausgewählt werden kann)</span><span class="sxs-lookup"><span data-stu-id="a2c52-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="a2c52-125">Lokale (Tiefe 1, auswählbar)</span><span class="sxs-lookup"><span data-stu-id="a2c52-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="a2c52-126">Ferngespräche (Tiefe 1, auswählbar)</span><span class="sxs-lookup"><span data-stu-id="a2c52-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a2c52-127">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a2c52-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a2c52-128">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a2c52-128">Protocol specifications</span></span>

<span data-ttu-id="a2c52-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2c52-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2c52-130">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a2c52-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a2c52-131">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2c52-131">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2c52-132">Gibt die Eigenschaften und Operationen, die für Address Book Vorlagen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="a2c52-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a2c52-133">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a2c52-133">Header files</span></span>

<span data-ttu-id="a2c52-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a2c52-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="a2c52-135">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a2c52-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="a2c52-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a2c52-136">Mapitags.h</span></span>
  
> <span data-ttu-id="a2c52-137">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a2c52-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a2c52-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2c52-138">See also</span></span>



[<span data-ttu-id="a2c52-139">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="a2c52-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="a2c52-140">PidTagFolderType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a2c52-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="a2c52-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a2c52-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a2c52-142">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a2c52-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a2c52-143">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a2c52-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a2c52-144">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a2c52-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

