---
title: Tabellen und die Speicherauslastung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: afd69f5a3fff69f670d6be78ba4957307cdb6995
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436860"
---
# <a name="tables-and-memory-usage"></a><span data-ttu-id="30169-103">Tabellen und die Speicherauslastung</span><span class="sxs-lookup"><span data-stu-id="30169-103">Tables and memory usage</span></span>

<span data-ttu-id="30169-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30169-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30169-105">Ein wichtiges Problem im Zusammenhang mit dem Abrufen von Daten aus einer Tabelle ist die Speichernutzung.</span><span class="sxs-lookup"><span data-stu-id="30169-105">An important issue connected with retrieving data from a table is memory usage.</span></span> <span data-ttu-id="30169-106">Fehlender verfügbarer Arbeitsspeicher kann dazu führen, dass [IMAPITable::QueryRows](imapitable-queryrows.md) und [HrQueryAllRows](hrqueryallrows.md) fehlschlagen und weniger als die gewünschte Anzahl von Zeilen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="30169-106">Lack of available memory can cause [IMAPITable::QueryRows](imapitable-queryrows.md) and [HrQueryAllRows](hrqueryallrows.md) to fail, returning less than the desired number of rows.</span></span> <span data-ttu-id="30169-107">Die Entscheidung, welche Methode oder Funktion zum Abrufen von Tabellendaten verwendet werden soll, hängt davon ab, ob erwartet werden kann, dass die Tabelle in den Arbeitsspeicher passt, und ob dies nicht möglich ist, wenn ein Fehler akzeptabel ist.</span><span class="sxs-lookup"><span data-stu-id="30169-107">Deciding which method or function to use to retrieve table data depends on whether the table can be expected to fit in memory, and if it cannot, if failure is acceptable.</span></span> 
  
<span data-ttu-id="30169-108">Da es nicht immer einfach ist, die Datenmenge zu bestimmen, die gleichzeitig in den Arbeitsspeicher passt, bietet MAPI einige grundlegende Richtlinien für eine Clientanwendung oder einen Dienstanbieter, die folgen sollen.</span><span class="sxs-lookup"><span data-stu-id="30169-108">Because it is not always easy to determine the amount of data that will fit into memory at one time, MAPI provides some basic guidelines for a client application or service provider to follow.</span></span> <span data-ttu-id="30169-109">Denken Sie daran, dass es immer Ausnahmen gibt, basierend auf der jeweiligen Tabellenimplementierung und der Art und Weise, wie die zugrunde liegenden Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="30169-109">Remember that there are always exceptions, based on the particular table implementation and how the underlying data is stored.</span></span>
  
<span data-ttu-id="30169-110">Die folgenden Richtlinien können verwendet werden, um die Verwendung des Tabellenspeichers auszuwerten:</span><span class="sxs-lookup"><span data-stu-id="30169-110">The following guidelines can be used to evaluate table memory usage:</span></span>
  
- <span data-ttu-id="30169-111">Clients, die gelegentliche Arbeitsspeicherauslastungen im Megabytebereich tolerieren können und davon ausgehen können, dass sie keine Probleme haben, eine gesamte Tabelle in den Arbeitsspeicher zu lesen.</span><span class="sxs-lookup"><span data-stu-id="30169-111">Clients that can tolerate occasional working set memory usage in the megabyte range and can assume they will have no problems reading an entire table into memory.</span></span> 
    
- <span data-ttu-id="30169-112">Einschränkungen haben Auswirkungen auf die Verwendung des Arbeitsspeichers in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="30169-112">Restrictions have an affect on a table's usage of memory.</span></span> <span data-ttu-id="30169-113">Es ist zu erwarten, dass eine stark eingeschränkte Tabelle mit einer großen Anzahl von Zeilen, z. B. einer Inhaltstabelle, in den Arbeitsspeicher passt, während eine unbeschränkte große Tabelle in der Regel nicht möglich ist.</span><span class="sxs-lookup"><span data-stu-id="30169-113">A severely restricted table with an extensive number of rows, such as a contents table, can be expected to fit into memory while an unrestricted large table usually cannot.</span></span> 
    
- <span data-ttu-id="30169-114">Einige der Tabellen im Besitz von MAPI, z. B. Status-, Profil-, Nachrichtendienst-, Anbieter- und Nachrichtenspeichertabellen, passen in der Regel in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="30169-114">Several of the tables owned by MAPI such as the status, profile, message service, provider, and message store tables, will usually fit in memory.</span></span> <span data-ttu-id="30169-115">Dies sind im Allgemeinen kleine Tabellen.</span><span class="sxs-lookup"><span data-stu-id="30169-115">These are generally small tables.</span></span> <span data-ttu-id="30169-116">Es gibt jedoch Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="30169-116">However, there are exceptions.</span></span> <span data-ttu-id="30169-117">Beispielsweise kann ein serverbasierter Profilanbieter eine größere Profiltabelle generieren, die nicht passen kann.</span><span class="sxs-lookup"><span data-stu-id="30169-117">For example, a server-based profile provider might generate a larger profile table that will not be able to fit.</span></span>
    
<span data-ttu-id="30169-118">Um alle Zeilen aus einer Tabelle abzurufen, die problemlos in den Arbeitsspeicher passt, rufen Sie [HrQueryAllRows](hrqueryallrows.md)auf, und legen Sie die maximale Anzahl von Zeilen auf Null fest.</span><span class="sxs-lookup"><span data-stu-id="30169-118">To retrieve all of the rows from a table that will fit into memory with no problems, call [HrQueryAllRows](hrqueryallrows.md), setting the maximum number of rows to zero.</span></span>
  
<span data-ttu-id="30169-119">Um alle Zeilen aus einer Tabelle abzurufen, die möglicherweise nicht in den Arbeitsspeicher passt, wird ein Fehler generiert, indem **Sie HrQueryAllRows** aufrufen, um eine maximale Anzahl von Zeilen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="30169-119">To retrieve all of the rows from a table that might or might not fit into memory, generating an error, call **HrQueryAllRows** specifying a maximum number of rows.</span></span> <span data-ttu-id="30169-120">Die maximale Anzahl von Zeilen sollte auf eine Zahl festgelegt werden, die größer als die mindestanzahl der erforderlichen Zeilen ist.</span><span class="sxs-lookup"><span data-stu-id="30169-120">The maximum number of rows should be set to a number greater than the minimum number of rows that are needed.</span></span> <span data-ttu-id="30169-121">Wenn ein Client aus einer 300-Zeilentabelle auf mindestens 50 Zeilen zugreifen muss, sollte die maximale Anzahl von Zeilen auf mindestens 51 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="30169-121">If a client must access at least 50 rows from a 300 row table, the maximum number of rows should be set to at least 51.</span></span> 
  
<span data-ttu-id="30169-122">Um alle Zeilen aus einer Tabelle abzurufen, die nicht in den Arbeitsspeicher passen soll, rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md) in einer Schleife mit einer relativ kleinen Zeilenanzahl auf, wie im folgenden Codebeispiel veranschaulicht wird:</span><span class="sxs-lookup"><span data-stu-id="30169-122">To retrieve all of the rows from a table that is not expected to fit into memory, call [IMAPITable::QueryRows](imapitable-queryrows.md) in a loop with a relatively small row count, as the following code sample illustrates:</span></span> 
  
```cpp
HRESULT     hr;
LPSRowSet   pRows = NULL;
LONG        irow;
LONG            cAsk = 50;                  // adjust this value
while ((hr = pTable->QueryRows(cAsk, 0, &pRows)) == hrSuccess
        && pRows->cRows != 0)
{
    for (irow = 0; irow < prows->cRows; ++irow)
    {
        // process the row...
    }
    FreeProws(pRows);
    pRows = NULL;
}
if (hr)
{
    // handle the error...
}
 
```

<span data-ttu-id="30169-123">Wenn diese Schleife abgeschlossen ist und alle Zeilen in der Tabelle verarbeitet wurden und  _cRows_ null ist, befindet sich die Position des Cursors in der Regel am unteren Rand der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="30169-123">When this loop completes and all the rows in the table have been processed and  _cRows_ is zero, the position of the cursor will usually be at the bottom of the table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="30169-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30169-124">See also</span></span>

- [<span data-ttu-id="30169-125">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="30169-125">MAPI Tables</span></span>](mapi-tables.md)

