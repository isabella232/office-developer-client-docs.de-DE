---
title: Sortieren und die Kategorisierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Zuletzt geändert: 08 November 2011'
ms.openlocfilehash: 5e63d276d25a26f937e9b4f44575fea1030f52d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795586"
---
# <a name="sorting-and-categorization"></a><span data-ttu-id="8c357-103">Sortieren und die Kategorisierung</span><span class="sxs-lookup"><span data-stu-id="8c357-103">Sorting and Categorization</span></span>

 
  
<span data-ttu-id="8c357-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8c357-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8c357-105">Sortieren einer Tabelle platziert Zeilen in einer Bestellung, die für den Viewer sinnvoll sind.</span><span class="sxs-lookup"><span data-stu-id="8c357-105">Sorting a table places rows in an order that makes sense for its viewer.</span></span> <span data-ttu-id="8c357-106">Angenommen, möchten ein Betrachter finden in der Inhaltstabelle eines Ordners sortiert nach Betreff der Nachricht, damit alle Threads einer Unterhaltung beieinander während einer anderen Viewer die Nachrichten, die nach dem Namen des Absenders sortiert sollten.</span><span class="sxs-lookup"><span data-stu-id="8c357-106">For example, one viewer might prefer to see the contents table of a folder sorted by message subject so that all the threads of a conversation are together while another viewer might want the messages sorted by the name of the sender.</span></span> <span data-ttu-id="8c357-107">Eine Tabelle neu instanziierte ist nicht unbedingt in einer bestimmten Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="8c357-107">A newly instantiated table is not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="8c357-108">Es gibt zwei Arten von sortieren:</span><span class="sxs-lookup"><span data-stu-id="8c357-108">There are two types of sorting:</span></span>
  
- <span data-ttu-id="8c357-109">Standard-Sortierung</span><span class="sxs-lookup"><span data-stu-id="8c357-109">Standard sorting</span></span>
    
- <span data-ttu-id="8c357-110">Kategorisiert sortieren</span><span class="sxs-lookup"><span data-stu-id="8c357-110">Categorized sorting</span></span> 
    
<span data-ttu-id="8c357-111">Mit standard sortieren, werden alle Zeilen in einer flachen Liste mit einer oder mehreren Spalten als Sortierschlüssel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c357-111">With standard sorting, all of the rows are displayed in a flat list using one or more columns as a sort key.</span></span> <span data-ttu-id="8c357-112">Mit kategorisierten sortieren, werden die Zeilen mit einer oder mehreren Spalten als Sortierschlüssel hierarchisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c357-112">With categorized sorting, the rows are displayed hierarchically with one or more columns as the sort key.</span></span> <span data-ttu-id="8c357-113">Innerhalb jeder Kategorie ist eine spezielle Überschriftenzeile, die die folgenden Spalten enthält.</span><span class="sxs-lookup"><span data-stu-id="8c357-113">Within each category, there is a special heading row that contains the following columns.</span></span>
  
- <span data-ttu-id="8c357-114">Die Spalte oder Spalten, die den Sortierschlüssel bilden</span><span class="sxs-lookup"><span data-stu-id="8c357-114">The column or columns that make up the sort key</span></span>
    
- <span data-ttu-id="8c357-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8c357-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="8c357-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8c357-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="8c357-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8c357-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="8c357-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8c357-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="8c357-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8c357-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span></span> 
    
<span data-ttu-id="8c357-120">Unter der Überschriftszeile eingezogen werden alle Zeilen aus der Tabelle, die Spalten mit Werten enthalten, die mit den Sortierschlüssel übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="8c357-120">Indented under the heading row are all the rows from the table that contain columns with values that match the sort key.</span></span> <span data-ttu-id="8c357-121">Diese Zeilen werden die Zeilen Endknoten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8c357-121">These rows are called the leaf rows.</span></span> <span data-ttu-id="8c357-122">Endknoten Zeilen enthalten alle Spalten in der Spalte minus Sortierschlüsselspalten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8c357-122">Leaf rows contain all the columns in the column set minus the sort key columns.</span></span> 
  
<span data-ttu-id="8c357-123">In den Tabellen Inhalt von Ordnern unterstützen häufig kategorisierte Sortierung zusätzlich zum standard sortieren.</span><span class="sxs-lookup"><span data-stu-id="8c357-123">The contents tables of folders often support categorized sorting in addition to standard sorting.</span></span> <span data-ttu-id="8c357-124">In den Tabellen Inhalt der Address Book Container unterstützen in der Regel nur standard sortieren.</span><span class="sxs-lookup"><span data-stu-id="8c357-124">The contents tables of address book containers typically support only standard sorting.</span></span> 
  
<span data-ttu-id="8c357-125">Eine Kategorie kann zwei Zustände haben: reduziert und erweitert.</span><span class="sxs-lookup"><span data-stu-id="8c357-125">A category can have two states: collapsed and expanded.</span></span> <span data-ttu-id="8c357-126">Wenn eine Kategorie im reduzierten Zustand befindet, wird nur die Kopfzeile von [IMAPITable::QueryRows](imapitable-queryrows.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8c357-126">When a category is in the collapsed state, only the heading row is returned from [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="8c357-127">Wenn eine Kategorie im erweiterten Zustand befindet, werden alle Zeilen im Zusammenhang mit der Kategorie zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8c357-127">When a category is in the expanded state, all of the rows related to the category are returned.</span></span> <span data-ttu-id="8c357-128">Dazu gehören die Kopfzeile und die untergeordneten Zeilen.</span><span class="sxs-lookup"><span data-stu-id="8c357-128">This includes the heading row and the leaf rows.</span></span> 
  
<span data-ttu-id="8c357-129">Jeder Kategorie in einer Tabellenansicht kann erweitert oder reduziert unabhängig voneinander.</span><span class="sxs-lookup"><span data-stu-id="8c357-129">Each category in a table view can be expanded or collapsed independently.</span></span> <span data-ttu-id="8c357-130">D. h., müssen nicht alle Kategorien in dem Zustand zur selben Zeit sein. Einige Kategorien können reduziert werden, während andere erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="8c357-130">That is, not all categories must be in the same state at the same time; some categories can be collapsed while others are expanded.</span></span> 
  
<span data-ttu-id="8c357-131">Der Benutzer einer kategorisierten Tabelle entscheidet, wie es angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8c357-131">The user of a categorized table decides how it is displayed.</span></span> <span data-ttu-id="8c357-132">Option für eine gemeinsame ist die Verwendung ein Steuerelements im Windows SDK bezeichnet das Treeview-Steuerelement bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8c357-132">One common option is to use a control provided in the Windows SDK called the treeview control.</span></span> <span data-ttu-id="8c357-133">TreeView-Steuerelemente sind Listenfelder, die Informationen in einer Baumstruktur unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8c357-133">Treeview controls are list boxes that support information in a tree-like structure.</span></span> <span data-ttu-id="8c357-134">Überschriftenzeilen für Kategorien im erweiterten Zustand werden mit einem Minuszeichen gekennzeichnet, während Überschriftenzeilen für Kategorien im reduzierten Zustand mit einem Pluszeichen (+) markiert sind.</span><span class="sxs-lookup"><span data-stu-id="8c357-134">Heading rows for categories in the expanded state are marked with a minus sign while heading rows for categories in the collapsed state are marked with a plus sign.</span></span> <span data-ttu-id="8c357-135">Mit den Endknoten Zeilen unter der Überschriftenzeilen eingezogen werden erweiterte Kategorien angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c357-135">Expanded categories are displayed with the leaf rows indented under the heading rows.</span></span> 
  
<span data-ttu-id="8c357-136">Um zu reduzieren und erweitern eine Kategorie, eine Clientanwendung oder Service Provider verwendet die folgenden [IMAPITable: IUnknown](imapitableiunknown.md) Methoden:</span><span class="sxs-lookup"><span data-stu-id="8c357-136">To collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span></span> 
  
- [<span data-ttu-id="8c357-137">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="8c357-137">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
    
- [<span data-ttu-id="8c357-138">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="8c357-138">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
    
- [<span data-ttu-id="8c357-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="8c357-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- [<span data-ttu-id="8c357-140">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="8c357-140">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
    
<span data-ttu-id="8c357-141">Weitere Informationen zum Sortieren der Threads einer Unterhaltung finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="8c357-141">For more information about sorting the threads of a conversation see the following topics:</span></span>
  
- [<span data-ttu-id="8c357-142">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="8c357-142">SSortOrder</span></span>](ssortorder.md)
    
- [<span data-ttu-id="8c357-143">Kanonische PidTagSubject-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8c357-143">PidTagSubject Canonical Property</span></span>](pidtagsubject-canonical-property.md)
    
- [<span data-ttu-id="8c357-144">Kanonische PidTagSubjectPrefix-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8c357-144">PidTagSubjectPrefix Canonical Property</span></span>](pidtagsubjectprefix-canonical-property.md)
    
- [<span data-ttu-id="8c357-145">Kanonische PidTagNormalizedSubject-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8c357-145">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
    
- [<span data-ttu-id="8c357-146">Kanonische Eigenschaftpidtagconversationtopic-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8c357-146">PidTagConversationTopic Canonical Property</span></span>](pidtagconversationtopic-canonical-property.md)
    
- [<span data-ttu-id="8c357-147">Kanonische-Eigenschaft PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="8c357-147">PidTagConversationIndex Canonical Property</span></span>](pidtagconversationindex-canonical-property.md)
    
- [<span data-ttu-id="8c357-148">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="8c357-148">ScCreateConversationIndex</span></span>](sccreateconversationindex.md)
    
- [<span data-ttu-id="8c357-149">Sortieren von Tabellen nach dem Festlegen der Spalten und Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="8c357-149">Sorting Tables After Setting Columns and Restrictions</span></span>](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a><span data-ttu-id="8c357-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c357-150">See also</span></span>



[<span data-ttu-id="8c357-151">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="8c357-151">MAPI Tables</span></span>](mapi-tables.md)

