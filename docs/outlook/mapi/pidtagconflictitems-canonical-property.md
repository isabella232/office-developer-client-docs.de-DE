---
title: Kanonische PidTagConflictItems-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 61176ec6f9ff00fa5a38a2b385cb5281fa40961e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794166"
---
# <a name="pidtagconflictitems-canonical-property"></a><span data-ttu-id="a82d8-103">Kanonische PidTagConflictItems-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a82d8-103">PidTagConflictItems Canonical Property</span></span>

  
  
<span data-ttu-id="a82d8-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a82d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a82d8-105">Enthält eine oder mehrere Eintrags-IDs der Elemente, die in einer automatischen Konfliktbehebung beteiligt waren.</span><span class="sxs-lookup"><span data-stu-id="a82d8-105">Contains one or more entry IDs of items that have been involved in an automatic conflict resolution.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="a82d8-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a82d8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a82d8-107">PR_CONFLICT_ITEMS</span><span class="sxs-lookup"><span data-stu-id="a82d8-107">PR_CONFLICT_ITEMS</span></span>  <br/> |
|<span data-ttu-id="a82d8-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="a82d8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a82d8-109">0x1098</span><span class="sxs-lookup"><span data-stu-id="a82d8-109">0x1098</span></span>  <br/> |
|<span data-ttu-id="a82d8-110">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="a82d8-110">Property type:</span></span>  <br/> |<span data-ttu-id="a82d8-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="a82d8-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="a82d8-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a82d8-112">Area:</span></span>  <br/> |<span data-ttu-id="a82d8-113">ICS</span><span class="sxs-lookup"><span data-stu-id="a82d8-113">ICS</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a82d8-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a82d8-114">Remarks</span></span>

<span data-ttu-id="a82d8-115">Typen von standard Microsoft Outlook-Elementen, die automatische Konfliktbehebung unterstützen die folgenden standardmäßigen Elementtypen enthalten: Terminelemente, Kontaktelementen, Journalelemente, e-Mail-Elementen, Elemente der Besprechung, Kurznotiz Elemente und Aufgabenelementen.</span><span class="sxs-lookup"><span data-stu-id="a82d8-115">The types of standard Microsoft Outlook items that support automatic conflict resolution include the following standard item types: appointment items, contact items, journal items, mail items, meeting items, sticky note items, and task items.</span></span> <span data-ttu-id="a82d8-116">Ein Element zu einer Nachrichtenklasse, die auch von einer der folgenden standardmäßigen Elementtypen abgeleitet ist gehören unterstützt automatische Konfliktbehebung.</span><span class="sxs-lookup"><span data-stu-id="a82d8-116">An item belonging to a message class that derives from one of these standard item types also supports automatic conflict resolution.</span></span> <span data-ttu-id="a82d8-117">In Microsoft Outlook 2003 und Microsoft Office Outlook 2007 Wenn Outlook Elemente synchronisiert und Auffassung besteht die Möglichkeit, dass die resultierende Kopie möglicherweise keine alle wichtige Daten enthalten, speichert Outlook die miteinander in Konflikt stehende Kopien in der **Konflikte** Ordner unterhalb des Ordners **Synchronisierungsprobleme** .</span><span class="sxs-lookup"><span data-stu-id="a82d8-117">In Microsoft Outlook 2003 and Microsoft Office Outlook 2007, when Outlook synchronizes items and considers that there is a possibility that the resultant copy may not contain all essential data, Outlook stores the conflicting copies in the **Conflicts** folder, under the **Sync Issues** folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a82d8-118">**Synchronisierungsprobleme** und den zugehörigen Unterordnern sind ausgeblendet, bis Sie im Menü **Gehe zu** auf **Ordnerliste** klicken.</span><span class="sxs-lookup"><span data-stu-id="a82d8-118">**Sync Issues** and its subfolders are hidden until you click **Folder List** on the **Go** menu.</span></span> 
  
<span data-ttu-id="a82d8-119">Ein Element wird die **PR_CONFLICT_ITEMS** -Eigenschaft verfügbar gemacht, wenn gehört zu den Elementtypen, die automatische Konfliktbehebung unterstützen, einen Konfliktbehebung gewonnen hat oder wurde im Ordner **Konflikte** aufgrund einer Konfliktbehebung platziert.</span><span class="sxs-lookup"><span data-stu-id="a82d8-119">An item exposes the **PR_CONFLICT_ITEMS** property if it is one of the item types that support automatic conflict resolution, has won in a conflict resolution, or was placed in the **Conflicts** folder because of a conflict resolution.</span></span> <span data-ttu-id="a82d8-120">Der Ordner, in dem das Element verschoben wird, bestimmt den Inhalt der **PR_CONFLICT_ITEMS**.</span><span class="sxs-lookup"><span data-stu-id="a82d8-120">The folder in which the item is placed determines the content of **PR_CONFLICT_ITEMS**.</span></span> <span data-ttu-id="a82d8-121">Wenn das Element sich im einige Ordner als dem Ordner **Konflikte befindet** und das Element die **PR_CONFLICT_ITEMS** -Eigenschaft macht, der Artikel muss die Konfliktbehebung erworben haben und **PR_CONFLICT_ITEMS** würde eine oder mehrere EntryIDs von Diese Elemente, die in der Konfliktbehebung verloren.</span><span class="sxs-lookup"><span data-stu-id="a82d8-121">If the item is located in some folder other than the **Conflicts** folder, and the item exposes the **PR_CONFLICT_ITEMS** property, the item must have won the conflict resolution, and **PR_CONFLICT_ITEMS** would contain one or more entry IDs of those items that lost in the conflict resolution.</span></span> <span data-ttu-id="a82d8-122">Wenn das Element sich im Ordner **Konflikte befindet** und das Element wird die **PR_CONFLICT_ITEMS** -Eigenschaft verfügbar gemacht, dieses Element muss die Konfliktbehebung verloren haben und **PR_CONFLICT_ITEMS** würde die Eintrags-ID des Elements, das in den Konflikt gewonnen Auflösung.</span><span class="sxs-lookup"><span data-stu-id="a82d8-122">If the item is located in the **Conflicts** folder and the item exposes the **PR_CONFLICT_ITEMS** property, this item must have lost the conflict resolution, and **PR_CONFLICT_ITEMS** would contain the entry ID of the item that won in the conflict resolution.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a82d8-123">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a82d8-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a82d8-124">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a82d8-124">Protocol specifications</span></span>

<span data-ttu-id="a82d8-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a82d8-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a82d8-126">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a82d8-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a82d8-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a82d8-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a82d8-128">Synchronisieren von messaging Objektdaten zwischen einem Server und einem Client behandelt.</span><span class="sxs-lookup"><span data-stu-id="a82d8-128">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a82d8-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a82d8-129">Header files</span></span>

<span data-ttu-id="a82d8-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a82d8-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="a82d8-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a82d8-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="a82d8-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a82d8-132">Mapitags.h</span></span>
  
> <span data-ttu-id="a82d8-133">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a82d8-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a82d8-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a82d8-134">See also</span></span>



[<span data-ttu-id="a82d8-135">Informationen zu MAPI-Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="a82d8-135">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="a82d8-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a82d8-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a82d8-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a82d8-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a82d8-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a82d8-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a82d8-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a82d8-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

