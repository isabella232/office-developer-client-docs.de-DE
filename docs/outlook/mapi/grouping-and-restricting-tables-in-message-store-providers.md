---
title: Gruppieren und Einschränken von Tabellen in Nachrichtenanbietern Store Anbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8a45a9fd0d40c16d110fd52be1ac1117e1dd4d04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428984"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a><span data-ttu-id="5232c-103">Gruppieren und Einschränken von Tabellen in Nachrichtenanbietern Store Anbieter</span><span class="sxs-lookup"><span data-stu-id="5232c-103">Grouping and Restricting Tables in Message Store Providers</span></span>

  
  
<span data-ttu-id="5232c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5232c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5232c-105">Clientanwendungen ermöglichen Benutzern häufig eine gewisse Kontrolle darüber, wie der Inhalt eines Ordners angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5232c-105">Client applications frequently allow users some control over how the contents of a folder are displayed.</span></span> <span data-ttu-id="5232c-106">In der Regel kann ein Benutzer festlegen, dass Nachrichten nach dem Wert einer oder mehreren Nachrichteneigenschaften gruppieren oder Nachrichten ausschließen, die bestimmten Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5232c-106">Typically, a user can choose to have messages grouped according to the value of one or more message properties, or can choose to exclude messages that match certain criteria.</span></span> <span data-ttu-id="5232c-107">Dies erfolgt mithilfe der [IMAPITable : IUnknown-Schnittstelle.](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="5232c-107">This is done by using the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="5232c-108">Clientanwendungen können die aus der Tabelle zurückgegebenen Zeilen auf die vom Benutzer angegebenen Kriterien beschränken.</span><span class="sxs-lookup"><span data-stu-id="5232c-108">Client applications can restrict the rows returned from the table to whatever criteria the user specifies.</span></span> <span data-ttu-id="5232c-109">Daher muss ein Nachrichtenspeicheranbieter die folgenden **IMAPITable-Methoden** implementieren.</span><span class="sxs-lookup"><span data-stu-id="5232c-109">Therefore, a message store provider needs to implement the following **IMAPITable** methods.</span></span> 
  
|<span data-ttu-id="5232c-110">IMAPITable**-Methode**</span><span class="sxs-lookup"><span data-stu-id="5232c-110">\*\*\*\*IMAPITable\*\* method\*\*</span></span>|<span data-ttu-id="5232c-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5232c-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5232c-112">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="5232c-112">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="5232c-113">Gibt Tabellenzeilen zurück, die den angegebenen Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5232c-113">Returns table rows that match the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="5232c-114">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="5232c-114">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="5232c-115">Gibt den Satz von Spalten in einer Tabelle oder den Satz der derzeit verwendeten Spalten zurück.</span><span class="sxs-lookup"><span data-stu-id="5232c-115">Returns the set of columns in a table or the set of currently used columns.</span></span>  <br/> |
|[<span data-ttu-id="5232c-116">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="5232c-116">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="5232c-117">Gibt eine oder mehrere Zeilen aus einer Tabelle ab einer bestimmten Position zurück.</span><span class="sxs-lookup"><span data-stu-id="5232c-117">Returns one or more rows from a table, starting from a given position.</span></span>  <br/> |
|[<span data-ttu-id="5232c-118">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="5232c-118">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="5232c-119">Wendet eine Einschränkung auf eine Tabelle an, sodass nachfolgende Aufrufe von **FindRow** nur Zeilen zurückgeben, die der Einschränkung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5232c-119">Applies a restriction to a table so that subsequent calls to **FindRow** return only rows that match the restriction.</span></span>  <br/> |
|[<span data-ttu-id="5232c-120">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="5232c-120">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="5232c-121">Gibt an, welche Spalten zurückgegeben werden sollen, wenn Zeilen aus der Tabelle abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5232c-121">Specifies which columns should be returned when rows are retrieved from the table.</span></span>  <br/> |
   
<span data-ttu-id="5232c-122">Einschränkungen können komplex implementiert werden. Weitere Informationen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="5232c-122">Restrictions can be complex to implement; for more information, see [About Restrictions](about-restrictions.md).</span></span> <span data-ttu-id="5232c-123">Weitere Informationen zum Implementieren von Tabellen finden Sie unter [MAPI Tables](mapi-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5232c-123">For more information about implementing tables, see [MAPI Tables](mapi-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5232c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5232c-124">See also</span></span>



[<span data-ttu-id="5232c-125">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="5232c-125">Message Store Features</span></span>](message-store-features.md)

