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
ms.openlocfilehash: 17343a721cbcc642c8cffe95112f25710c0c130c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359017"
---
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="8439b-103">PidTagSelectable (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8439b-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="8439b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8439b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8439b-105">Enthält TRUE, wenn der Eintrag in der einmal aufgeführten Tabelle ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8439b-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8439b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8439b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8439b-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="8439b-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="8439b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8439b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8439b-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="8439b-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="8439b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8439b-110">Data type:</span></span>  <br/> |<span data-ttu-id="8439b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8439b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8439b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8439b-112">Area:</span></span>  <br/> |<span data-ttu-id="8439b-113">Adressbuchcontainer</span><span class="sxs-lookup"><span data-stu-id="8439b-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8439b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8439b-114">Remarks</span></span>

<span data-ttu-id="8439b-115">Diese Eigenschaft wird hauptsächlich für die visuelle Formatierung einer einmal verwendeten Tabelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="8439b-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="8439b-116">Vorlagen können durch Erstellen eines Eintrags, der die Überschrift für die Gruppe angibt, gruppieren.</span><span class="sxs-lookup"><span data-stu-id="8439b-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="8439b-117">Durch Festlegen dieser Eigenschaft auf FALSE für die Überschrift wird sichergestellt, dass der Benutzer nur die tatsächlichen Vorlagen in der Gruppe und nicht diesen Überschrifteneintrag auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="8439b-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="8439b-118">Diese Eigenschaft gilt nur für eine Einmaltabelle und nicht für eine Adressbuchhierarchietabelle.</span><span class="sxs-lookup"><span data-stu-id="8439b-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="8439b-119">MAPI ermöglicht es einem Adressbuchanbieter, Elemente auf zwei Arten visuell zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="8439b-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="8439b-120">Zunächst können bestimmte Zeilen als Überschriften funktionieren, indem sie nicht ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="8439b-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="8439b-121">Zweitens können die auswählbaren Elemente relativ zu ihren Überschriften mithilfe der **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) eingezogen werden.</span><span class="sxs-lookup"><span data-stu-id="8439b-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="8439b-122">Diese Eigenschaft wird in einer solchen Gruppierung verwendet, um anzugeben, ob dieses Element aus einer Liste ausgewählt werden kann, um eine einmal verwendete Adresse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8439b-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="8439b-123">Wenn ein Client beispielsweise über mehrere Vorlagen zum Erstellen von Faxadressen verfügt, kann er diese wie folgt anzeigen:</span><span class="sxs-lookup"><span data-stu-id="8439b-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="8439b-124">FAXvorlagen (Tiefe 0, nicht auswählbar)</span><span class="sxs-lookup"><span data-stu-id="8439b-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="8439b-125">Lokal (Tiefe 1, auswählbar)</span><span class="sxs-lookup"><span data-stu-id="8439b-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="8439b-126">Long-Distance (Tiefe 1, auswählbar)</span><span class="sxs-lookup"><span data-stu-id="8439b-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8439b-127">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8439b-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8439b-128">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8439b-128">Protocol specifications</span></span>

<span data-ttu-id="8439b-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8439b-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8439b-130">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8439b-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8439b-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8439b-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8439b-132">Gibt die Eigenschaften und Vorgänge an, die für Adressbuchvorlagen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="8439b-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8439b-133">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="8439b-133">Header files</span></span>

<span data-ttu-id="8439b-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8439b-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="8439b-135">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8439b-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="8439b-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8439b-136">Mapitags.h</span></span>
  
> <span data-ttu-id="8439b-137">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8439b-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8439b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8439b-138">See also</span></span>



[<span data-ttu-id="8439b-139">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="8439b-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="8439b-140">PidTagFolderType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8439b-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="8439b-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8439b-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8439b-142">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="8439b-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8439b-143">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8439b-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8439b-144">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8439b-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

