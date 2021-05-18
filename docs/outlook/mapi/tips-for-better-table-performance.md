---
title: Tipps für eine bessere Tabellenleistung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 82be33090a63f24c430007d9759045c365961f5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412513"
---
# <a name="tips-for-better-table-performance"></a><span data-ttu-id="58272-103">Tipps für eine bessere Tabellenleistung</span><span class="sxs-lookup"><span data-stu-id="58272-103">Tips for better table performance</span></span>
  
<span data-ttu-id="58272-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58272-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58272-105">Da viele Tabellenvorgänge zeitaufwändig sein können und keine Möglichkeit zum Angeben des Fortschritts besteht, ist es hilfreich, die folgenden Techniken zur Verbesserung der Leistung zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="58272-105">Because many of the table operations can be time-consuming and there is no way to indicate progress, it is helpful to use the following techniques for improving performance:</span></span>
  
- <span data-ttu-id="58272-106">**[ImAPITable erstellen: IUnknown-Aufrufe](imapitableiunknown.md) in der richtigen Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="58272-106">**Make [IMAPITable : IUnknown](imapitableiunknown.md) calls in the correct order**</span></span>
    
   <span data-ttu-id="58272-107">Clients und Dienstanbieter können auf unterschiedliche Weise mit Tabellen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="58272-107">Clients and service providers can work with tables in a variety of ways.</span></span> <span data-ttu-id="58272-108">Sie können die Tabelle öffnen und die Daten für alle Zeilen mithilfe der Standardspaltensatz- und Sortierreihenfolge abrufen.</span><span class="sxs-lookup"><span data-stu-id="58272-108">They can open the table and retrieve the data for all of the rows using the default column set and sort order.</span></span> <span data-ttu-id="58272-109">Alternativ können sie diese Standardansicht der Tabelle ändern, indem sie den Spaltensatz ändern, die Sortierreihenfolge ändern oder eine Einschränkung festlegen, um den Bereich der Tabelle zu einentwickeln.</span><span class="sxs-lookup"><span data-stu-id="58272-109">Alternatively, they can modify this default view of the table by changing the column set, changing the sort order, or establishing a restriction to narrow the table's scope.</span></span> <span data-ttu-id="58272-110">Tabellenbenutzer, die einen oder mehrere dieser Vorgänge vor dem Abrufen von Daten ausführen möchten, sollten diese in der folgenden Reihenfolge ausführen:</span><span class="sxs-lookup"><span data-stu-id="58272-110">Table users that intend to perform one or more of these operations before retrieving any data should perform them in the following order:</span></span>
    
    1. <span data-ttu-id="58272-111">Definieren sie einen Spaltensatz mit [IMAPITable::SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="58272-111">Define a column set with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
        
    2. <span data-ttu-id="58272-112">Richten Sie eine Einschränkung mit [IMAPITable::Restrict ein.](imapitable-restrict.md)</span><span class="sxs-lookup"><span data-stu-id="58272-112">Establish a restriction with [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
        
    3. <span data-ttu-id="58272-113">Definieren Einer Sortierreihenfolge mit [IMAPITable::SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="58272-113">Define a sort order with [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
    <span data-ttu-id="58272-114">Wenn Sie diese Aufgaben in dieser Reihenfolge ausführen, wird die Anzahl der Zeilen und Spalten begrenzt, die sortiert werden, wodurch die Leistung verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="58272-114">Performing these tasks in this order limits the number of rows and columns that will be sorted, thereby improving performance.</span></span>
    
- <span data-ttu-id="58272-115">**Verzögern eines Vorgangs mithilfe des TBL_BATCH, wenn möglich**</span><span class="sxs-lookup"><span data-stu-id="58272-115">**Delay an operation using the TBL_BATCH flag if possible**</span></span>
    
    <span data-ttu-id="58272-116">Durch Festlegen des TBL BATCH-Kennzeichens für eine Methode kann der Tabellen implementier mehrere Aufrufe sammeln, bevor er auf einen \_ dieser Aufrufe einwirken kann.</span><span class="sxs-lookup"><span data-stu-id="58272-116">Setting the TBL\_BATCH flag on a method allows the table implementer to collect several calls before acting on any one of them.</span></span> <span data-ttu-id="58272-117">Statt potenziell viele Aufrufe an einen Remoteserver zu senden; Ein Tabellen implementier kann eins erstellen und alle Vorgänge gleichzeitig ausführen.</span><span class="sxs-lookup"><span data-stu-id="58272-117">Instead of make potentially many calls to a remote server; a table implementer can make one, performing all the operations at one time.</span></span> <span data-ttu-id="58272-118">Die Ergebnisse der Vorgänge werden erst ausgewertet, wenn sie benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="58272-118">The results of the operations are not evaluated until they are needed.</span></span> 
    
    <span data-ttu-id="58272-119">Wenn ein Client beispielsweise [IMAPITable::Restrict](imapitable-restrict.md) aufruft, um eine Einschränkung mit dem TBL BATCH-Flagsatz anzugeben, muss die Einschränkung erst wirksam werden, wenn der Client \_ [IMAPITable::QueryRows](imapitable-queryrows.md) aufruft, um die Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="58272-119">For example, when a client calls [IMAPITable::Restrict](imapitable-restrict.md) to specify a restriction with the TBL\_BATCH flag set, the restriction do not have to go into effect until the client calls [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the data.</span></span> <span data-ttu-id="58272-120">Auf diese Weise kann der Tabellen implementier die Arbeit von zwei Aufrufen in einem kombinieren.</span><span class="sxs-lookup"><span data-stu-id="58272-120">This allows the table implementer to combine the work of two calls into one.</span></span> <span data-ttu-id="58272-121">Tabellenbenutzer, die das TBL BATCH-Flag nutzen, sollten beachten, dass die Fehlerbehandlung unter diesen Bedingungen \_ komplexer sein kann.</span><span class="sxs-lookup"><span data-stu-id="58272-121">Table users that take advantage of the TBL\_BATCH flag should be aware that error handling under these conditions can be more complex.</span></span> 
    
    <span data-ttu-id="58272-122">Da die Behandlung der Fehler eines verzögerten Vorgangs der Behandlung der Fehler ähnelt, wenn das MAPI-DEFERRED_ERRORS festgelegt ist, finden Sie weitere Informationen unter \_ [Deferring MAPI Errors.](deferring-mapi-errors.md)</span><span class="sxs-lookup"><span data-stu-id="58272-122">Because handling the errors from a delayed operation is similar to handling the errors when the MAPI\_DEFERRED_ERRORS flag is set, see [Deferring MAPI Errors](deferring-mapi-errors.md) for more information.</span></span> 
    
- <span data-ttu-id="58272-123">**Speichern eines Caches häufig verwendeter Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="58272-123">**Keep a cache of commonly used properties**</span></span>
    
    <span data-ttu-id="58272-124">Dienstanbieter, die Tabellen implementieren, können die Zeit zum Erstellen einer Ansicht durch Zwischenspeichern von Kopien häufig verwendeter Objekteigenschaften mindern.</span><span class="sxs-lookup"><span data-stu-id="58272-124">Service providers implementing tables can lessen the time it takes to create a view by caching copies of commonly used object properties.</span></span> <span data-ttu-id="58272-125">Wenn Sie eine Kopie dieser Eigenschaften im Arbeitsspeicher speichern, müssen sie jedes Mal aus dem Objekt abgerufen werden, wenn die Ansicht neu erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="58272-125">Keeping a copy of these properties in memory saves having to retrieve them from the object each time the view must be rebuilt.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58272-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58272-126">See also</span></span>

- [<span data-ttu-id="58272-127">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="58272-127">MAPI Tables</span></span>](mapi-tables.md)

