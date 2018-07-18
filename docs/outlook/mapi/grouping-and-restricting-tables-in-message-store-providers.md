---
title: Gruppieren und Einschränken von Tabellen in Nachrichtenspeicheranbietern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 33c76cdd0e7850f82949349ac2e5bb0dd4e056ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791795"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a><span data-ttu-id="3f261-103">Gruppieren und Einschränken von Tabellen in Nachrichtenspeicheranbietern</span><span class="sxs-lookup"><span data-stu-id="3f261-103">Grouping and Restricting Tables in Message Store Providers</span></span>

  
  
<span data-ttu-id="3f261-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3f261-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3f261-105">Clientanwendungen können Benutzer häufig besser steuern, wie der Inhalt eines Ordners angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3f261-105">Client applications frequently allow users some control over how the contents of a folder are displayed.</span></span> <span data-ttu-id="3f261-106">In der Regel ein Benutzer kann auswählen, dass Nachrichten entsprechend dem Wert der Nachrichteneigenschaften für eine oder mehrere gruppiert oder kann verhindern, dass Nachrichten auszuschließen, die bestimmte Kriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="3f261-106">Typically, a user can choose to have messages grouped according to the value of one or more message properties, or can choose to exclude messages that match certain criteria.</span></span> <span data-ttu-id="3f261-107">Dies erfolgt mithilfe der [IMAPITable: IUnknown](imapitableiunknown.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3f261-107">This is done by using the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="3f261-108">Clientanwendungen können einschränken, die Zeilen aus der Tabelle an beliebige erforderliche Kriterien gibt an, der Benutzer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3f261-108">Client applications can restrict the rows returned from the table to whatever criteria the user specifies.</span></span> <span data-ttu-id="3f261-109">Speichern Sie daher, eine Nachricht Anbieter muss die folgenden **IMAPITable** -Methoden implementieren.</span><span class="sxs-lookup"><span data-stu-id="3f261-109">Therefore, a message store provider needs to implement the following **IMAPITable** methods.</span></span> 
  
|<span data-ttu-id="3f261-110">IMAPITable **-Methode **</span><span class="sxs-lookup"><span data-stu-id="3f261-110">****IMAPITable** method**</span></span>|<span data-ttu-id="3f261-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3f261-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f261-112">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="3f261-112">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="3f261-113">Gibt die Tabelle Zeilen, die die angegebenen Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3f261-113">Returns table rows that match the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="3f261-114">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="3f261-114">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="3f261-115">Gibt die Gruppe von Spalten in einer Tabelle oder die Gruppe von aktuell verwendeten Spalten zurück.</span><span class="sxs-lookup"><span data-stu-id="3f261-115">Returns the set of columns in a table or the set of currently used columns.</span></span>  <br/> |
|[<span data-ttu-id="3f261-116">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="3f261-116">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="3f261-117">Gibt eine oder mehrere Zeilen aus einer Tabelle, beginnend mit einer bestimmten Position zurück.</span><span class="sxs-lookup"><span data-stu-id="3f261-117">Returns one or more rows from a table, starting from a given position.</span></span>  <br/> |
|[<span data-ttu-id="3f261-118">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="3f261-118">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="3f261-119">Wendet die Einschränkung, die einer Tabelle, sodass nachfolgende Aufrufe von **FindRow** nur Zeilen zurück, die der Einschränkung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3f261-119">Applies a restriction to a table so that subsequent calls to **FindRow** return only rows that match the restriction.</span></span>  <br/> |
|[<span data-ttu-id="3f261-120">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="3f261-120">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="3f261-121">Gibt an, welche Spalten zurückgegeben werden sollen, wenn Zeilen aus der Tabelle abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3f261-121">Specifies which columns should be returned when rows are retrieved from the table.</span></span>  <br/> |
   
<span data-ttu-id="3f261-122">Einschränkungen können zur Implementierung komplex sein; Weitere Informationen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="3f261-122">Restrictions can be complex to implement; for more information, see [About Restrictions](about-restrictions.md).</span></span> <span data-ttu-id="3f261-123">Weitere Informationen zum Implementieren der Tabellen finden Sie unter [MAPI-Tabellen](mapi-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3f261-123">For more information about implementing tables, see [MAPI Tables](mapi-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3f261-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f261-124">See also</span></span>



[<span data-ttu-id="3f261-125">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="3f261-125">Message Store Features</span></span>](message-store-features.md)

