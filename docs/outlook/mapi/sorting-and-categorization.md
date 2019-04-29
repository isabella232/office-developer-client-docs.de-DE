---
title: Sortieren und kategorisieren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Zuletzt geändert: 20 November, 2011'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418484"
---
# <a name="sorting-and-categorization"></a><span data-ttu-id="eefda-103">Sortieren und kategorisieren</span><span class="sxs-lookup"><span data-stu-id="eefda-103">Sorting and Categorization</span></span>

 
  
<span data-ttu-id="eefda-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eefda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eefda-105">Beim Sortieren einer Tabelle werden Zeilen in einer Reihenfolge platziert, die für den Betrachter sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="eefda-105">Sorting a table places rows in an order that makes sense for its viewer.</span></span> <span data-ttu-id="eefda-106">Beispielsweise könnte ein Betrachter die Inhaltstabelle eines Ordners nach Nachrichtenbetreff sortiert anzeigen, sodass alle Threads einer Unterhaltung zusammen sind, während ein anderer Betrachter die Nachrichten nach dem Namen des Absenders sortieren kann.</span><span class="sxs-lookup"><span data-stu-id="eefda-106">For example, one viewer might prefer to see the contents table of a folder sorted by message subject so that all the threads of a conversation are together while another viewer might want the messages sorted by the name of the sender.</span></span> <span data-ttu-id="eefda-107">Eine neu instanziierte Tabelle ist nicht unbedingt in einer bestimmten Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="eefda-107">A newly instantiated table is not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="eefda-108">Es gibt zwei Arten der Sortierung:</span><span class="sxs-lookup"><span data-stu-id="eefda-108">There are two types of sorting:</span></span>
  
- <span data-ttu-id="eefda-109">Standard Sortierung</span><span class="sxs-lookup"><span data-stu-id="eefda-109">Standard sorting</span></span>
    
- <span data-ttu-id="eefda-110">Kategorisierte Sortierung</span><span class="sxs-lookup"><span data-stu-id="eefda-110">Categorized sorting</span></span> 
    
<span data-ttu-id="eefda-111">Bei der Standardsortierung werden alle Zeilen in einer flachen Liste mit einer oder mehreren Spalten als Sortierschlüssel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eefda-111">With standard sorting, all of the rows are displayed in a flat list using one or more columns as a sort key.</span></span> <span data-ttu-id="eefda-112">Bei der kategorisierten Sortierung werden die Zeilen hierarchisch mit einer oder mehreren Spalten als Sortierschlüssel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eefda-112">With categorized sorting, the rows are displayed hierarchically with one or more columns as the sort key.</span></span> <span data-ttu-id="eefda-113">Innerhalb jeder Kategorie gibt es eine spezielle Überschriftenzeile mit den folgenden Spalten.</span><span class="sxs-lookup"><span data-stu-id="eefda-113">Within each category, there is a special heading row that contains the following columns.</span></span>
  
- <span data-ttu-id="eefda-114">Die Spalten, aus denen der Sortierschlüssel besteht</span><span class="sxs-lookup"><span data-stu-id="eefda-114">The column or columns that make up the sort key</span></span>
    
- <span data-ttu-id="eefda-115">**PR_CONTENT_COUNT** ([Pidtagcontentcount (](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefda-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="eefda-116">**PR_CONTENT_UNREAD** ([Pidtagcontentunreadcount (](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefda-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="eefda-117">**PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefda-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="eefda-118">**PR_DEPTH** ([Pidtagdepth (](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefda-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="eefda-119">**PR_ROW_TYPE** ([Pidtagrowtype (](pidtagrowtype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eefda-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span></span> 
    
<span data-ttu-id="eefda-120">Eingerückt unter der Überschriftenzeile befinden sich alle Zeilen aus der Tabelle, die Spalten mit Werten enthalten, die mit dem Sortierschlüssel übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="eefda-120">Indented under the heading row are all the rows from the table that contain columns with values that match the sort key.</span></span> <span data-ttu-id="eefda-121">Diese Zeilen werden als Blattzeilen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="eefda-121">These rows are called the leaf rows.</span></span> <span data-ttu-id="eefda-122">Blattzeilen enthalten alle Spalten in der Spaltengruppe minus der Sortierschlüsselspalten.</span><span class="sxs-lookup"><span data-stu-id="eefda-122">Leaf rows contain all the columns in the column set minus the sort key columns.</span></span> 
  
<span data-ttu-id="eefda-123">Die Inhaltsordner Verzeichnisse unterstützen häufig kategorisierte Sortierungen zusätzlich zur Standardsortierung.</span><span class="sxs-lookup"><span data-stu-id="eefda-123">The contents tables of folders often support categorized sorting in addition to standard sorting.</span></span> <span data-ttu-id="eefda-124">Die Inhaltstabellen der Adressbuchcontainer unterstützen in der Regel nur die Standardsortierung.</span><span class="sxs-lookup"><span data-stu-id="eefda-124">The contents tables of address book containers typically support only standard sorting.</span></span> 
  
<span data-ttu-id="eefda-125">Eine Kategorie kann zwei Zustände aufweisen: reduziert und erweitert.</span><span class="sxs-lookup"><span data-stu-id="eefda-125">A category can have two states: collapsed and expanded.</span></span> <span data-ttu-id="eefda-126">Wenn sich eine Kategorie im reduzierten Zustand befindet, wird nur die Überschriftenzeile von [IMAPITable:: QueryRows](imapitable-queryrows.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eefda-126">When a category is in the collapsed state, only the heading row is returned from [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="eefda-127">Wenn sich eine Kategorie im erweiterten Zustand befindet, werden alle mit der Kategorie verknüpften Zeilen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eefda-127">When a category is in the expanded state, all of the rows related to the category are returned.</span></span> <span data-ttu-id="eefda-128">Dazu gehören die Überschriftenzeile und die Blattzeilen.</span><span class="sxs-lookup"><span data-stu-id="eefda-128">This includes the heading row and the leaf rows.</span></span> 
  
<span data-ttu-id="eefda-129">Jede Kategorie in einer Tabellenansicht kann unabhängig voneinander erweitert oder reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="eefda-129">Each category in a table view can be expanded or collapsed independently.</span></span> <span data-ttu-id="eefda-130">Das heißt, nicht alle Kategorien müssen gleichzeitig in demselben Zustand sein; Einige Kategorien können reduziert werden, während andere erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="eefda-130">That is, not all categories must be in the same state at the same time; some categories can be collapsed while others are expanded.</span></span> 
  
<span data-ttu-id="eefda-131">Der Benutzer einer kategorisierten Tabelle entscheidet, wie er angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="eefda-131">The user of a categorized table decides how it is displayed.</span></span> <span data-ttu-id="eefda-132">Eine gängige Option ist die Verwendung eines Steuerelements, das im Windows SDK mit dem Namen TreeView-Steuerelement bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="eefda-132">One common option is to use a control provided in the Windows SDK called the treeview control.</span></span> <span data-ttu-id="eefda-133">TreeView-Steuerelemente sind Listenfelder, die Informationen in einer baumartigen Struktur unterstützen.</span><span class="sxs-lookup"><span data-stu-id="eefda-133">Treeview controls are list boxes that support information in a tree-like structure.</span></span> <span data-ttu-id="eefda-134">Überschriftenzeilen für Kategorien im erweiterten Zustand sind mit einem Minuszeichen gekennzeichnet, während Überschriftenzeilen für Kategorien im reduzierten Zustand mit einem Pluszeichen gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="eefda-134">Heading rows for categories in the expanded state are marked with a minus sign while heading rows for categories in the collapsed state are marked with a plus sign.</span></span> <span data-ttu-id="eefda-135">Erweiterte Kategorien werden mit eingezogenen Blattzeilen unter der Überschriftenzeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eefda-135">Expanded categories are displayed with the leaf rows indented under the heading rows.</span></span> 
  
<span data-ttu-id="eefda-136">Zum reduzieren und Erweitern einer Kategorie verwendet eine Clientanwendung oder ein Dienstanbieter die folgenden [IMAPITable: IUnknown](imapitableiunknown.md) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="eefda-136">To collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span></span> 
  
- [<span data-ttu-id="eefda-137">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="eefda-137">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
    
- [<span data-ttu-id="eefda-138">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="eefda-138">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
    
- [<span data-ttu-id="eefda-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="eefda-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- [<span data-ttu-id="eefda-140">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="eefda-140">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
    
<span data-ttu-id="eefda-141">Weitere Informationen zum Sortieren der Threads einer Unterhaltung finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="eefda-141">For more information about sorting the threads of a conversation see the following topics:</span></span>
  
- [<span data-ttu-id="eefda-142">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="eefda-142">SSortOrder</span></span>](ssortorder.md)
    
- [<span data-ttu-id="eefda-143">Kanonische PidTagSubject-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eefda-143">PidTagSubject Canonical Property</span></span>](pidtagsubject-canonical-property.md)
    
- [<span data-ttu-id="eefda-144">Kanonische Pidtagsubjectprefix (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eefda-144">PidTagSubjectPrefix Canonical Property</span></span>](pidtagsubjectprefix-canonical-property.md)
    
- [<span data-ttu-id="eefda-145">Kanonische PidTagNormalizedSubject-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eefda-145">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
    
- [<span data-ttu-id="eefda-146">Kanonische Eigenschaftpidtagconversationtopic-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eefda-146">PidTagConversationTopic Canonical Property</span></span>](pidtagconversationtopic-canonical-property.md)
    
- [<span data-ttu-id="eefda-147">Kanonische PidTagConversationIndex-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eefda-147">PidTagConversationIndex Canonical Property</span></span>](pidtagconversationindex-canonical-property.md)
    
- [<span data-ttu-id="eefda-148">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="eefda-148">ScCreateConversationIndex</span></span>](sccreateconversationindex.md)
    
- [<span data-ttu-id="eefda-149">Sortieren von Tabellen nach dem Festlegen von Spalten und Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="eefda-149">Sorting Tables After Setting Columns and Restrictions</span></span>](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a><span data-ttu-id="eefda-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eefda-150">See also</span></span>



[<span data-ttu-id="eefda-151">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="eefda-151">MAPI Tables</span></span>](mapi-tables.md)

