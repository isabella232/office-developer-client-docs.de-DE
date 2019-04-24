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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327797"
---
# <a name="tips-for-better-table-performance"></a><span data-ttu-id="a5531-103">Tipps für eine bessere Tabellenleistung</span><span class="sxs-lookup"><span data-stu-id="a5531-103">Tips for better table performance</span></span>
  
<span data-ttu-id="a5531-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5531-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5531-105">Da viele der Tabellenvorgänge zeitaufwändig sein können und es keine Möglichkeit gibt, den Fortschritt anzugeben, empfiehlt es sich, die folgenden Techniken zur Verbesserung der Leistung zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="a5531-105">Because many of the table operations can be time-consuming and there is no way to indicate progress, it is helpful to use the following techniques for improving performance:</span></span>
  
- <span data-ttu-id="a5531-106">**Make [IMAPITable: IUnknown](imapitableiunknown.md) Calls in der richtigen Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="a5531-106">**Make [IMAPITable : IUnknown](imapitableiunknown.md) calls in the correct order**</span></span>
    
   <span data-ttu-id="a5531-107">Clients und Dienstanbieter können mit Tabellen auf verschiedene Arten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a5531-107">Clients and service providers can work with tables in a variety of ways.</span></span> <span data-ttu-id="a5531-108">Sie können die Tabelle öffnen und die Daten für alle Zeilen mit dem standardmäßigen Spaltensatz und der Sortierreihenfolge abrufen.</span><span class="sxs-lookup"><span data-stu-id="a5531-108">They can open the table and retrieve the data for all of the rows using the default column set and sort order.</span></span> <span data-ttu-id="a5531-109">Alternativ können Sie diese Standardansicht der Tabelle ändern, indem Sie den Spaltensatz ändern, die Sortierreihenfolge ändern oder eine Einschränkung einrichten, um den Bereich der Tabelle einzugrenzen.</span><span class="sxs-lookup"><span data-stu-id="a5531-109">Alternatively, they can modify this default view of the table by changing the column set, changing the sort order, or establishing a restriction to narrow the table's scope.</span></span> <span data-ttu-id="a5531-110">Tabellen Benutzer, die einen oder mehrere dieser Vorgänge vor dem Abrufen von Daten ausführen möchten, sollten diese in der folgenden Reihenfolge ausführen:</span><span class="sxs-lookup"><span data-stu-id="a5531-110">Table users that intend to perform one or more of these operations before retrieving any data should perform them in the following order:</span></span>
    
    1. <span data-ttu-id="a5531-111">Definieren Sie einen Spaltensatz mit [IMAPITable::](imapitable-setcolumns.md)SetColumns.</span><span class="sxs-lookup"><span data-stu-id="a5531-111">Define a column set with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
        
    2. <span data-ttu-id="a5531-112">Richten Sie eine Einschränkung mit [IMAPITable:: Restrict](imapitable-restrict.md)ein.</span><span class="sxs-lookup"><span data-stu-id="a5531-112">Establish a restriction with [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
        
    3. <span data-ttu-id="a5531-113">Definieren Sie eine Sortierreihenfolge mit [IMAPITable:: sortable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="a5531-113">Define a sort order with [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
    <span data-ttu-id="a5531-114">Wenn Sie diese Aufgaben in dieser Reihenfolge durchführen, wird die Anzahl der Zeilen und Spalten begrenzt, die sortiert werden, wodurch die Leistung verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="a5531-114">Performing these tasks in this order limits the number of rows and columns that will be sorted, thereby improving performance.</span></span>
    
- <span data-ttu-id="a5531-115">**VerZögern eines Vorgangs mit dem TBL_BATCH-Flag, wenn möglich**</span><span class="sxs-lookup"><span data-stu-id="a5531-115">**Delay an operation using the TBL_BATCH flag if possible**</span></span>
    
    <span data-ttu-id="a5531-116">Das Festlegen des\_TBL-Batch-Flags für eine Methode ermöglicht es der Tabellen Implementierung, mehrere Aufrufe zu sammeln, bevor Sie auf eine dieser Methoden reagieren.</span><span class="sxs-lookup"><span data-stu-id="a5531-116">Setting the TBL\_BATCH flag on a method allows the table implementer to collect several calls before acting on any one of them.</span></span> <span data-ttu-id="a5531-117">Statt potenziell viele Aufrufe an einen Remoteserver zu senden; eine Tabellen Implementierung kann eine erstellen, die alle Vorgänge gleichzeitig ausführt.</span><span class="sxs-lookup"><span data-stu-id="a5531-117">Instead of make potentially many calls to a remote server; a table implementer can make one, performing all the operations at one time.</span></span> <span data-ttu-id="a5531-118">Die Ergebnisse der Vorgänge werden erst ausgewertet, wenn Sie benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="a5531-118">The results of the operations are not evaluated until they are needed.</span></span> 
    
    <span data-ttu-id="a5531-119">Wenn ein Client beispielsweise [IMAPITable:: Restrict](imapitable-restrict.md) anruft, um eine Einschränkung mit der TBL\_-Batch-flaggruppe anzugeben, muss die Einschränkung erst wirksam werden, wenn der Client [IMAPITable:: QueryRows](imapitable-queryrows.md) zum Abrufen der Daten aufruft.</span><span class="sxs-lookup"><span data-stu-id="a5531-119">For example, when a client calls [IMAPITable::Restrict](imapitable-restrict.md) to specify a restriction with the TBL\_BATCH flag set, the restriction do not have to go into effect until the client calls [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the data.</span></span> <span data-ttu-id="a5531-120">Dies ermöglicht es der Tabellen Implementierung, die Arbeit zweier Aufrufe zu einem zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="a5531-120">This allows the table implementer to combine the work of two calls into one.</span></span> <span data-ttu-id="a5531-121">Tabellen Benutzer, die das TBL\_-Batch-Flag nutzen, sollten beachten, dass die Fehlerbehandlung unter diesen Bedingungen komplexer sein kann.</span><span class="sxs-lookup"><span data-stu-id="a5531-121">Table users that take advantage of the TBL\_BATCH flag should be aware that error handling under these conditions can be more complex.</span></span> 
    
    <span data-ttu-id="a5531-122">Da die Behandlung von Fehlern aus einem verzögerten Vorgang mit dem Behandeln der Fehler vergleichbar ist\_, wenn das MAPI-DEFERRED_ERRORS-Flag festgelegt ist, finden Sie weitere Informationen unter Zurückstellen von [MAPI-Fehlern](deferring-mapi-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="a5531-122">Because handling the errors from a delayed operation is similar to handling the errors when the MAPI\_DEFERRED_ERRORS flag is set, see [Deferring MAPI Errors](deferring-mapi-errors.md) for more information.</span></span> 
    
- <span data-ttu-id="a5531-123">**Speichern eines Caches häufig verwendeter Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="a5531-123">**Keep a cache of commonly used properties**</span></span>
    
    <span data-ttu-id="a5531-124">Dienstanbieter, die Tabellen implementieren, können die Zeit zum Erstellen einer Ansicht verringern, indem Sie Kopien der häufig verwendeten Objekteigenschaften Zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="a5531-124">Service providers implementing tables can lessen the time it takes to create a view by caching copies of commonly used object properties.</span></span> <span data-ttu-id="a5531-125">Wenn Sie eine Kopie dieser Eigenschaften im Arbeitsspeicher behalten, müssen Sie jedes Mal aus dem Objekt abgerufen werden, wenn die Ansicht neu erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="a5531-125">Keeping a copy of these properties in memory saves having to retrieve them from the object each time the view must be rebuilt.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5531-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5531-126">See also</span></span>

- [<span data-ttu-id="a5531-127">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="a5531-127">MAPI Tables</span></span>](mapi-tables.md)

