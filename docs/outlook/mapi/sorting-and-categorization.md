---
title: Sortieren und Kategorisieren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Letzte Änderung: 08. November 2011'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418484"
---
# <a name="sorting-and-categorization"></a><span data-ttu-id="67398-103">Sortieren und Kategorisieren</span><span class="sxs-lookup"><span data-stu-id="67398-103">Sorting and Categorization</span></span>

 
  
<span data-ttu-id="67398-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67398-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67398-105">Beim Sortieren einer Tabelle werden Zeilen in einer Reihenfolge platziert, die für den Viewer sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="67398-105">Sorting a table places rows in an order that makes sense for its viewer.</span></span> <span data-ttu-id="67398-106">Ein Betrachter möchte beispielsweise das Inhaltsverzeichnis eines Ordners nach Nachrichtenbe betreff sortiert sehen, sodass alle Threads einer Unterhaltung zusammengef?ndet werden, während ein anderer Benutzer die Nachrichten nach dem Namen des Absenders sortieren möchte.</span><span class="sxs-lookup"><span data-stu-id="67398-106">For example, one viewer might prefer to see the contents table of a folder sorted by message subject so that all the threads of a conversation are together while another viewer might want the messages sorted by the name of the sender.</span></span> <span data-ttu-id="67398-107">Eine neu instanziierte Tabelle ist nicht unbedingt in einer bestimmten Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="67398-107">A newly instantiated table is not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="67398-108">Es gibt zwei Arten von Sortierung:</span><span class="sxs-lookup"><span data-stu-id="67398-108">There are two types of sorting:</span></span>
  
- <span data-ttu-id="67398-109">Standardsortierung</span><span class="sxs-lookup"><span data-stu-id="67398-109">Standard sorting</span></span>
    
- <span data-ttu-id="67398-110">Kategorisierte Sortierung</span><span class="sxs-lookup"><span data-stu-id="67398-110">Categorized sorting</span></span> 
    
<span data-ttu-id="67398-111">Bei der Standardsortierung werden alle Zeilen in einer flachen Liste mit einer oder mehreren Spalten als Sortierschlüssel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="67398-111">With standard sorting, all of the rows are displayed in a flat list using one or more columns as a sort key.</span></span> <span data-ttu-id="67398-112">Bei der kategorisierten Sortierung werden die Zeilen hierarchisch mit einer oder mehreren Spalten als Sortierschlüssel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="67398-112">With categorized sorting, the rows are displayed hierarchically with one or more columns as the sort key.</span></span> <span data-ttu-id="67398-113">In jeder Kategorie befindet sich eine spezielle Überschriftenzeile, die die folgenden Spalten enthält.</span><span class="sxs-lookup"><span data-stu-id="67398-113">Within each category, there is a special heading row that contains the following columns.</span></span>
  
- <span data-ttu-id="67398-114">Die Spalte oder Spalten, aus der der Sortierschlüssel ist</span><span class="sxs-lookup"><span data-stu-id="67398-114">The column or columns that make up the sort key</span></span>
    
- <span data-ttu-id="67398-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="67398-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="67398-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="67398-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="67398-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="67398-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="67398-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="67398-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="67398-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="67398-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span></span> 
    
<span data-ttu-id="67398-120">Eingerückt unter der Überschriftenzeile sind alle Zeilen aus der Tabelle, die Spalten mit Werten enthalten, die mit dem Sortierschlüssel übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="67398-120">Indented under the heading row are all the rows from the table that contain columns with values that match the sort key.</span></span> <span data-ttu-id="67398-121">Diese Zeilen werden als Blattzeilen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="67398-121">These rows are called the leaf rows.</span></span> <span data-ttu-id="67398-122">Blattzeilen enthalten alle Spalten im Spaltensatz minus der Sortierschlüsselspalten.</span><span class="sxs-lookup"><span data-stu-id="67398-122">Leaf rows contain all the columns in the column set minus the sort key columns.</span></span> 
  
<span data-ttu-id="67398-123">Die Inhaltstabellen von Ordnern unterstützen häufig die kategorisierte Sortierung zusätzlich zur Standardsortierung.</span><span class="sxs-lookup"><span data-stu-id="67398-123">The contents tables of folders often support categorized sorting in addition to standard sorting.</span></span> <span data-ttu-id="67398-124">Die Inhaltstabellen von Adressbuchcontainern unterstützen in der Regel nur die Standardsortierung.</span><span class="sxs-lookup"><span data-stu-id="67398-124">The contents tables of address book containers typically support only standard sorting.</span></span> 
  
<span data-ttu-id="67398-125">Eine Kategorie kann zwei Zustände haben: reduziert und erweitert.</span><span class="sxs-lookup"><span data-stu-id="67398-125">A category can have two states: collapsed and expanded.</span></span> <span data-ttu-id="67398-126">Wenn sich eine Kategorie im reduzierten Zustand befindet, wird nur die Überschriftenzeile von [IMAPITable::QueryRows zurückgegeben.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="67398-126">When a category is in the collapsed state, only the heading row is returned from [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="67398-127">Wenn sich eine Kategorie im erweiterten Zustand befindet, werden alle zeilen im Zusammenhang mit der Kategorie zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="67398-127">When a category is in the expanded state, all of the rows related to the category are returned.</span></span> <span data-ttu-id="67398-128">Dies umfasst die Überschriftenzeile und die Blattzeilen.</span><span class="sxs-lookup"><span data-stu-id="67398-128">This includes the heading row and the leaf rows.</span></span> 
  
<span data-ttu-id="67398-129">Jede Kategorie in einer Tabellenansicht kann unabhängig voneinander erweitert oder reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="67398-129">Each category in a table view can be expanded or collapsed independently.</span></span> <span data-ttu-id="67398-130">Das heißt, nicht alle Kategorien müssen gleichzeitig denselben Status haben. Einige Kategorien können reduziert werden, während andere erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="67398-130">That is, not all categories must be in the same state at the same time; some categories can be collapsed while others are expanded.</span></span> 
  
<span data-ttu-id="67398-131">Der Benutzer einer kategorisierten Tabelle entscheidet, wie sie angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="67398-131">The user of a categorized table decides how it is displayed.</span></span> <span data-ttu-id="67398-132">Eine gängige Option ist die Verwendung eines Steuerelements, das im Windows SDK als Strukturansichtssteuerelement bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="67398-132">One common option is to use a control provided in the Windows SDK called the treeview control.</span></span> <span data-ttu-id="67398-133">Strukturansichtssteuerelemente sind Listenfelder, die Informationen in einer struktur like structure unterstützen.</span><span class="sxs-lookup"><span data-stu-id="67398-133">Treeview controls are list boxes that support information in a tree-like structure.</span></span> <span data-ttu-id="67398-134">Überschriftenzeilen für Kategorien im erweiterten Zustand werden mit einem Minuszeichen markiert, während Überschriftenzeilen für Kategorien im reduzierten Zustand mit einem Pluszeichen markiert sind.</span><span class="sxs-lookup"><span data-stu-id="67398-134">Heading rows for categories in the expanded state are marked with a minus sign while heading rows for categories in the collapsed state are marked with a plus sign.</span></span> <span data-ttu-id="67398-135">Erweiterte Kategorien werden angezeigt, wenn die Blattzeilen unter den Überschriftenzeilen eingezogen sind.</span><span class="sxs-lookup"><span data-stu-id="67398-135">Expanded categories are displayed with the leaf rows indented under the heading rows.</span></span> 
  
<span data-ttu-id="67398-136">Um eine Kategorie zu reduzieren und zu erweitern, verwendet eine Clientanwendung oder ein Dienstanbieter die folgenden [IMAPITable-Methoden: IUnknown-Methoden:](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="67398-136">To collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span></span> 
  
- [<span data-ttu-id="67398-137">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="67398-137">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
    
- [<span data-ttu-id="67398-138">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="67398-138">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
    
- [<span data-ttu-id="67398-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="67398-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- [<span data-ttu-id="67398-140">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="67398-140">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
    
<span data-ttu-id="67398-141">Weitere Informationen zum Sortieren der Threads einer Unterhaltung finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="67398-141">For more information about sorting the threads of a conversation see the following topics:</span></span>
  
- [<span data-ttu-id="67398-142">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="67398-142">SSortOrder</span></span>](ssortorder.md)
    
- [<span data-ttu-id="67398-143">PidTagSubject (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="67398-143">PidTagSubject Canonical Property</span></span>](pidtagsubject-canonical-property.md)
    
- [<span data-ttu-id="67398-144">PidTagSubjectPrefix (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="67398-144">PidTagSubjectPrefix Canonical Property</span></span>](pidtagsubjectprefix-canonical-property.md)
    
- [<span data-ttu-id="67398-145">PidTagNormalizedSubject (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="67398-145">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
    
- [<span data-ttu-id="67398-146">PidTagConversationTopic (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="67398-146">PidTagConversationTopic Canonical Property</span></span>](pidtagconversationtopic-canonical-property.md)
    
- [<span data-ttu-id="67398-147">PidTagConversationIndex (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="67398-147">PidTagConversationIndex Canonical Property</span></span>](pidtagconversationindex-canonical-property.md)
    
- [<span data-ttu-id="67398-148">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="67398-148">ScCreateConversationIndex</span></span>](sccreateconversationindex.md)
    
- [<span data-ttu-id="67398-149">Sortieren von Tabellen nach dem Festlegen von Spalten und Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="67398-149">Sorting Tables After Setting Columns and Restrictions</span></span>](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a><span data-ttu-id="67398-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67398-150">See also</span></span>



[<span data-ttu-id="67398-151">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="67398-151">MAPI Tables</span></span>](mapi-tables.md)

