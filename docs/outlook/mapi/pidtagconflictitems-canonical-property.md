---
title: PidTagConflictItems (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConflictItems
api_type:
- HeaderDef
ms.assetid: 0d147827-f0e2-dcc1-4427-c4a2f48ca801
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 83940d9239bc172d5fab76232f6644f0e89033b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338017"
---
# <a name="pidtagconflictitems-canonical-property"></a><span data-ttu-id="195a2-103">PidTagConflictItems (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="195a2-103">PidTagConflictItems Canonical Property</span></span>

  
  
<span data-ttu-id="195a2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="195a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="195a2-105">Enthält eine oder mehrere Eintrags-IDs von Elementen, die an einer automatischen Konfliktlösung beteiligt waren.</span><span class="sxs-lookup"><span data-stu-id="195a2-105">Contains one or more entry IDs of items that have been involved in an automatic conflict resolution.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="195a2-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="195a2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="195a2-107">PR_CONFLICT_ITEMS</span><span class="sxs-lookup"><span data-stu-id="195a2-107">PR_CONFLICT_ITEMS</span></span>  <br/> |
|<span data-ttu-id="195a2-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="195a2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="195a2-109">0x1098</span><span class="sxs-lookup"><span data-stu-id="195a2-109">0x1098</span></span>  <br/> |
|<span data-ttu-id="195a2-110">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="195a2-110">Property type:</span></span>  <br/> |<span data-ttu-id="195a2-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="195a2-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="195a2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="195a2-112">Area:</span></span>  <br/> |<span data-ttu-id="195a2-113">ICS</span><span class="sxs-lookup"><span data-stu-id="195a2-113">ICS</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="195a2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="195a2-114">Remarks</span></span>

<span data-ttu-id="195a2-115">Die Typen von standardmäßigen Microsoft Outlook-Elementen, die die automatische Konfliktlösung unterstützen, umfassen die folgenden Standardelementtypen: Terminelemente, Kontaktelemente, Journalelemente, E-Mail-Elemente, Besprechungselemente, Notizelemente und Aufgabenelemente.</span><span class="sxs-lookup"><span data-stu-id="195a2-115">The types of standard Microsoft Outlook items that support automatic conflict resolution include the following standard item types: appointment items, contact items, journal items, mail items, meeting items, sticky note items, and task items.</span></span> <span data-ttu-id="195a2-116">Ein Element einer Nachrichtenklasse, das von einem dieser Standardelementtypen ab leitet, unterstützt auch die automatische Konfliktlösung.</span><span class="sxs-lookup"><span data-stu-id="195a2-116">An item belonging to a message class that derives from one of these standard item types also supports automatic conflict resolution.</span></span> <span data-ttu-id="195a2-117">Wenn Outlook in Microsoft Outlook 2003 und Microsoft Office Outlook 2007 Elemente synchronisiert und der Ansicht ist, dass die sich ausdingende Kopie möglicherweise nicht alle wichtigen  Daten enthält,  speichert Outlook die in Konflikt konfliktenden Kopien im Ordner Konflikte unter dem Ordner Synchronisierungsprobleme.</span><span class="sxs-lookup"><span data-stu-id="195a2-117">In Microsoft Outlook 2003 and Microsoft Office Outlook 2007, when Outlook synchronizes items and considers that there is a possibility that the resultant copy may not contain all essential data, Outlook stores the conflicting copies in the **Conflicts** folder, under the **Sync Issues** folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="195a2-118">**Sync Issues** and its subfolders are hidden until you click **Folder List** on the **Go** menu.</span><span class="sxs-lookup"><span data-stu-id="195a2-118">**Sync Issues** and its subfolders are hidden until you click **Folder List** on the **Go** menu.</span></span> 
  
<span data-ttu-id="195a2-119">Ein Element macht die **PR_CONFLICT_ITEMS-Eigenschaft** verfügbar, wenn es sich um einen der Elementtypen handelt, die die  automatische Konfliktlösung unterstützen, in einer Konfliktlösung gewonnen haben oder aufgrund einer Konfliktauflösung im Ordner Konflikte platziert wurden.</span><span class="sxs-lookup"><span data-stu-id="195a2-119">An item exposes the **PR_CONFLICT_ITEMS** property if it is one of the item types that support automatic conflict resolution, has won in a conflict resolution, or was placed in the **Conflicts** folder because of a conflict resolution.</span></span> <span data-ttu-id="195a2-120">Der Ordner, in dem das Element platziert wird, bestimmt den Inhalt **PR_CONFLICT_ITEMS.**</span><span class="sxs-lookup"><span data-stu-id="195a2-120">The folder in which the item is placed determines the content of **PR_CONFLICT_ITEMS**.</span></span> <span data-ttu-id="195a2-121">Wenn sich das Element in einem  anderen Ordner als dem Ordner Konflikte befindet und das Element die **PR_CONFLICT_ITEMS-Eigenschaft** verfügbar macht, muss das Element die Konfliktauflösung gewonnen haben, und **PR_CONFLICT_ITEMS** würde eine oder mehrere Eintrags-IDs dieser Elemente enthalten, die in der Konfliktlösung verloren gegangen sind.</span><span class="sxs-lookup"><span data-stu-id="195a2-121">If the item is located in some folder other than the **Conflicts** folder, and the item exposes the **PR_CONFLICT_ITEMS** property, the item must have won the conflict resolution, and **PR_CONFLICT_ITEMS** would contain one or more entry IDs of those items that lost in the conflict resolution.</span></span> <span data-ttu-id="195a2-122">Wenn sich das Element  im Ordner Konflikte befindet und das Element die **PR_CONFLICT_ITEMS-Eigenschaft** verfügbar macht, muss dieses Element die Konfliktauflösung verloren haben, und **PR_CONFLICT_ITEMS** würde die Eintrags-ID des Elements enthalten, das in der Konfliktauflösung gewonnen wurde.</span><span class="sxs-lookup"><span data-stu-id="195a2-122">If the item is located in the **Conflicts** folder and the item exposes the **PR_CONFLICT_ITEMS** property, this item must have lost the conflict resolution, and **PR_CONFLICT_ITEMS** would contain the entry ID of the item that won in the conflict resolution.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="195a2-123">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="195a2-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="195a2-124">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="195a2-124">Protocol specifications</span></span>

<span data-ttu-id="195a2-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="195a2-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="195a2-126">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="195a2-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="195a2-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="195a2-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="195a2-128">Behandelt die Synchronisierung von Messagingobjektdaten zwischen einem Server und einem Client.</span><span class="sxs-lookup"><span data-stu-id="195a2-128">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="195a2-129">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="195a2-129">Header files</span></span>

<span data-ttu-id="195a2-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="195a2-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="195a2-131">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="195a2-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="195a2-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="195a2-132">Mapitags.h</span></span>
  
> <span data-ttu-id="195a2-133">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="195a2-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="195a2-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="195a2-134">See also</span></span>



[<span data-ttu-id="195a2-135">Informationen zu MAPI-Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="195a2-135">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="195a2-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="195a2-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="195a2-137">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="195a2-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="195a2-138">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="195a2-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="195a2-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="195a2-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

