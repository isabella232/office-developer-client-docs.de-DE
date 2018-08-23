---
title: Tipps zur Leistungssteigerung-Tabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: da49b4d8251f6b0b69d2ffbf80194943215675e2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564164"
---
# <a name="tips-for-better-table-performance"></a><span data-ttu-id="329fa-103">Tipps zur Leistungssteigerung-Tabelle</span><span class="sxs-lookup"><span data-stu-id="329fa-103">Tips for better table performance</span></span>
  
<span data-ttu-id="329fa-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="329fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="329fa-105">Da viele Tabellenvorgänge zeitaufwendig sein können und es nicht möglich ist, Status anzugeben, ist es hilfreich, die folgenden Techniken zur Verbesserung der Leistung verwenden:</span><span class="sxs-lookup"><span data-stu-id="329fa-105">Because many of the table operations can be time-consuming and there is no way to indicate progress, it is helpful to use the following techniques for improving performance:</span></span>
  
- <span data-ttu-id="329fa-106">**Stellen Sie [IMAPITable: IUnknown](imapitableiunknown.md) ruft in der richtigen Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="329fa-106">**Make [IMAPITable : IUnknown](imapitableiunknown.md) calls in the correct order**</span></span>
    
   <span data-ttu-id="329fa-107">Clients und Dienstanbieter können mit Tabellen in verschiedene Arten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="329fa-107">Clients and service providers can work with tables in a variety of ways.</span></span> <span data-ttu-id="329fa-108">Sie können öffnen Sie die Tabelle und die Daten für alle Zeilen mit dem Spalte Standardsatz abruft und Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="329fa-108">They can open the table and retrieve the data for all of the rows using the default column set and sort order.</span></span> <span data-ttu-id="329fa-109">Alternativ können sie diese Standardansicht der Tabelle ändern, indem die Spalte Set ändern, Ändern der Sortierreihenfolge oder zur Festlegung einer Einschränkung, um die Tabelle zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="329fa-109">Alternatively, they can modify this default view of the table by changing the column set, changing the sort order, or establishing a restriction to narrow the table's scope.</span></span> <span data-ttu-id="329fa-110">Benutzer, die eine oder mehrere der folgenden Vorgänge ausführen, bevor Sie Daten abrufen möchten, sollten sie in der folgenden Reihenfolge ausführen:</span><span class="sxs-lookup"><span data-stu-id="329fa-110">Table users that intend to perform one or more of these operations before retrieving any data should perform them in the following order:</span></span>
    
    1. <span data-ttu-id="329fa-111">Definieren Sie eine Spalte mit [IMAPITable::SetColumns](imapitable-setcolumns.md)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="329fa-111">Define a column set with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
        
    2. <span data-ttu-id="329fa-112">Richten Sie eine Einschränkung mit [Methode IMAPITable:: Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="329fa-112">Establish a restriction with [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
        
    3. <span data-ttu-id="329fa-113">Definieren Sie eine Sortierreihenfolge mit [SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="329fa-113">Define a sort order with [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
    <span data-ttu-id="329fa-114">Diese Aufgaben in der angegebenen Reihenfolge beschränkt die Anzahl der Zeilen und Spalten, die sortiert werden soll, wodurch die Leistung verbessert.</span><span class="sxs-lookup"><span data-stu-id="329fa-114">Performing these tasks in this order limits the number of rows and columns that will be sorted, thereby improving performance.</span></span>
    
- <span data-ttu-id="329fa-115">**Verzögerung für einen Vorgang Wenn möglich mit dem TBL_BATCH-flag**</span><span class="sxs-lookup"><span data-stu-id="329fa-115">**Delay an operation using the TBL_BATCH flag if possible**</span></span>
    
    <span data-ttu-id="329fa-116">Festlegen der TBL\_BATCH-Flag für eine Methode kann in der Tabelle Implementierung mehrere Aufrufe vor dem Bearbeiten auf jedem dieser erfassen.</span><span class="sxs-lookup"><span data-stu-id="329fa-116">Setting the TBL\_BATCH flag on a method allows the table implementer to collect several calls before acting on any one of them.</span></span> <span data-ttu-id="329fa-117">Stellen Sie anstelle von potenziell viele Anrufe auf einem Remoteserver. eine Tabelle Implementierer kann, stellen Sie alle Vorgänge gleichzeitig durchführen.</span><span class="sxs-lookup"><span data-stu-id="329fa-117">Instead of make potentially many calls to a remote server; a table implementer can make one, performing all the operations at one time.</span></span> <span data-ttu-id="329fa-118">Die Ergebnisse der Vorgänge werden nicht ausgewertet, bis sie benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="329fa-118">The results of the operations are not evaluated until they are needed.</span></span> 
    
    <span data-ttu-id="329fa-119">Beispielsweise wenn ein Client ruft [Methode IMAPITable:: Restrict](imapitable-restrict.md) eine Einschränkung mit der TBL angeben\_BATCH-Kennzeichens, die Einschränkung müssen nicht wirksam, bis der Client [IMAPITable::QueryRows](imapitable-queryrows.md) zum Abrufen der Daten aufruft.</span><span class="sxs-lookup"><span data-stu-id="329fa-119">For example, when a client calls [IMAPITable::Restrict](imapitable-restrict.md) to specify a restriction with the TBL\_BATCH flag set, the restriction do not have to go into effect until the client calls [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the data.</span></span> <span data-ttu-id="329fa-120">Dies kann in der Tabelle-Implementierung die Arbeit in eine zwei Anrufe zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="329fa-120">This allows the table implementer to combine the work of two calls into one.</span></span> <span data-ttu-id="329fa-121">Benutzer, die die TBL nutzen Tabelle\_BATCH Flag sollten beachten Sie, dass unter diesen Umständen Fehlerbehandlung komplexer sein kann.</span><span class="sxs-lookup"><span data-stu-id="329fa-121">Table users that take advantage of the TBL\_BATCH flag should be aware that error handling under these conditions can be more complex.</span></span> 
    
    <span data-ttu-id="329fa-122">Da die Fehlerbehandlung von einer verzögerten Vorgang ähnelt der Fehlerbehandlung ist bei der MAPI\_DEFERRED_ERRORS Flag festgelegt ist, finden Sie weitere Informationen unter [Verzögern MAPI-Fehler](deferring-mapi-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="329fa-122">Because handling the errors from a delayed operation is similar to handling the errors when the MAPI\_DEFERRED_ERRORS flag is set, see [Deferring MAPI Errors](deferring-mapi-errors.md) for more information.</span></span> 
    
- <span data-ttu-id="329fa-123">**Lassen Sie einen Cache der am häufigsten verwendeten Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="329fa-123">**Keep a cache of commonly used properties**</span></span>
    
    <span data-ttu-id="329fa-124">Dienstanbieter implementieren Tabellen können die Zeit verringern, die benötigt wird, um eine Ansicht zu erstellen, indem zwischengespeichert werden Kopien der häufig verwendeten Objekteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="329fa-124">Service providers implementing tables can lessen the time it takes to create a view by caching copies of commonly used object properties.</span></span> <span data-ttu-id="329fa-125">Erstellen einer Kopie der diese Eigenschaften im Arbeitsspeicher speichert, müssen sie jedes Mal aus dem Objekt Abrufen der Ansicht muss neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="329fa-125">Keeping a copy of these properties in memory saves having to retrieve them from the object each time the view must be rebuilt.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="329fa-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="329fa-126">See also</span></span>

- [<span data-ttu-id="329fa-127">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="329fa-127">MAPI Tables</span></span>](mapi-tables.md)

