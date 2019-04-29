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
# <a name="tables-and-memory-usage"></a><span data-ttu-id="549d5-103">Tabellen und die Speicherauslastung</span><span class="sxs-lookup"><span data-stu-id="549d5-103">Tables and memory usage</span></span>

<span data-ttu-id="549d5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="549d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="549d5-105">Ein wichtiges Problem beim Abrufen von Daten aus einer Tabelle ist die Speicherauslastung.</span><span class="sxs-lookup"><span data-stu-id="549d5-105">An important issue connected with retrieving data from a table is memory usage.</span></span> <span data-ttu-id="549d5-106">Fehlender verfügbarer Arbeitsspeicher kann dazu führen, dass [IMAPITable:: QueryRows](imapitable-queryrows.md) und [HrQueryAllRows](hrqueryallrows.md) fehlschlägt, sodass weniger als die gewünschte Anzahl von Zeilen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="549d5-106">Lack of available memory can cause [IMAPITable::QueryRows](imapitable-queryrows.md) and [HrQueryAllRows](hrqueryallrows.md) to fail, returning less than the desired number of rows.</span></span> <span data-ttu-id="549d5-107">Die Entscheidung, welche Methode oder Funktion zum Abrufen von Tabellendaten verwendet werden kann, hängt davon ab, ob die Tabelle in den Arbeitsspeicher passt, und falls dies nicht möglich ist, wenn ein Fehlschlagen akzeptabel ist.</span><span class="sxs-lookup"><span data-stu-id="549d5-107">Deciding which method or function to use to retrieve table data depends on whether the table can be expected to fit in memory, and if it cannot, if failure is acceptable.</span></span> 
  
<span data-ttu-id="549d5-108">Da es nicht immer einfach ist, die Datenmenge zu bestimmen, die gleichzeitig in den Arbeitsspeicher passt, bietet MAPI einige grundlegende Richtlinien für eine Clientanwendung oder einen Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="549d5-108">Because it is not always easy to determine the amount of data that will fit into memory at one time, MAPI provides some basic guidelines for a client application or service provider to follow.</span></span> <span data-ttu-id="549d5-109">Denken Sie daran, dass es immer Ausnahmen gibt, die auf der jeweiligen Tabellen Implementierung basieren und wie die zugrunde liegenden Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="549d5-109">Remember that there are always exceptions, based on the particular table implementation and how the underlying data is stored.</span></span>
  
<span data-ttu-id="549d5-110">Die folgenden Richtlinien können zum Auswerten der Tabellenspeicher Verwendung verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="549d5-110">The following guidelines can be used to evaluate table memory usage:</span></span>
  
- <span data-ttu-id="549d5-111">Clients, die gelegentlich Arbeitsspeicherauslastung im megabytebereich tolerieren können und davon ausgehen, dass Sie keine Probleme beim Lesen einer gesamten Tabelle in den Arbeitsspeicher haben.</span><span class="sxs-lookup"><span data-stu-id="549d5-111">Clients that can tolerate occasional working set memory usage in the megabyte range and can assume they will have no problems reading an entire table into memory.</span></span> 
    
- <span data-ttu-id="549d5-112">Einschränkungen wirken sich auf die Speicherbelegung einer Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="549d5-112">Restrictions have an affect on a table's usage of memory.</span></span> <span data-ttu-id="549d5-113">Eine stark eingeschränkte Tabelle mit einer umfangreichen Anzahl von Zeilen, wie etwa einer Inhaltstabelle, kann voraussichtlich in den Arbeitsspeicher integriert werden, während eine uneingeschränkte große Tabelle in der Regel nicht möglich ist.</span><span class="sxs-lookup"><span data-stu-id="549d5-113">A severely restricted table with an extensive number of rows, such as a contents table, can be expected to fit into memory while an unrestricted large table usually cannot.</span></span> 
    
- <span data-ttu-id="549d5-114">Einige der Tabellen, die MAPI gehören, wie Status-, Profil-, Nachrichtendienst-, Anbieter-und nachrichtenspeichertabellen, werden in der Regel in den Arbeitsspeicher passt.</span><span class="sxs-lookup"><span data-stu-id="549d5-114">Several of the tables owned by MAPI such as the status, profile, message service, provider, and message store tables, will usually fit in memory.</span></span> <span data-ttu-id="549d5-115">Hierbei handelt es sich im Allgemeinen um kleine Tabellen.</span><span class="sxs-lookup"><span data-stu-id="549d5-115">These are generally small tables.</span></span> <span data-ttu-id="549d5-116">Es gibt jedoch Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="549d5-116">However, there are exceptions.</span></span> <span data-ttu-id="549d5-117">Ein serverbasierter Profilanbieter kann beispielsweise eine größere Profiltabelle generieren, die nicht angepasst werden kann.</span><span class="sxs-lookup"><span data-stu-id="549d5-117">For example, a server-based profile provider might generate a larger profile table that will not be able to fit.</span></span>
    
<span data-ttu-id="549d5-118">Wenn Sie alle Zeilen aus einer Tabelle abrufen möchten, die ohne Probleme in den Arbeitsspeicher passt, rufen Sie [HrQueryAllRows](hrqueryallrows.md)auf, und legen Sie die maximale Anzahl von Zeilen auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="549d5-118">To retrieve all of the rows from a table that will fit into memory with no problems, call [HrQueryAllRows](hrqueryallrows.md), setting the maximum number of rows to zero.</span></span>
  
<span data-ttu-id="549d5-119">Wenn Sie alle Zeilen aus einer Tabelle abrufen möchten, die möglicherweise nicht in den Arbeitsspeicher passt, und einen Fehler generiert, rufen Sie **HrQueryAllRows** auf, um eine maximale Anzahl von Zeilen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="549d5-119">To retrieve all of the rows from a table that might or might not fit into memory, generating an error, call **HrQueryAllRows** specifying a maximum number of rows.</span></span> <span data-ttu-id="549d5-120">Die maximale Anzahl von Zeilen sollte auf eine Zahl festgelegt werden, die größer ist als die Mindestanzahl der benötigten Zeilen.</span><span class="sxs-lookup"><span data-stu-id="549d5-120">The maximum number of rows should be set to a number greater than the minimum number of rows that are needed.</span></span> <span data-ttu-id="549d5-121">Wenn ein Client auf mindestens 50 Zeilen aus einer 300-Zeilentabelle zugreifen muss, sollte die maximale Anzahl von Zeilen auf mindestens 51 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="549d5-121">If a client must access at least 50 rows from a 300 row table, the maximum number of rows should be set to at least 51.</span></span> 
  
<span data-ttu-id="549d5-122">Wenn Sie alle Zeilen aus einer Tabelle abrufen möchten, die nicht in den Arbeitsspeicher passt, rufen Sie [IMAPITable:: QueryRows](imapitable-queryrows.md) in einer Schleife mit einer relativ kleinen Zeilenanzahl auf, wie im folgenden Codebeispiel veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="549d5-122">To retrieve all of the rows from a table that is not expected to fit into memory, call [IMAPITable::QueryRows](imapitable-queryrows.md) in a loop with a relatively small row count, as the following code sample illustrates:</span></span> 
  
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

<span data-ttu-id="549d5-123">Wenn diese Schleife abgeschlossen ist und alle Zeilen in der Tabelle verarbeitet wurden und _Crows_ gleich NULL ist, wird die Position des Cursors in der Regel am unteren Rand der Tabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="549d5-123">When this loop completes and all the rows in the table have been processed and  _cRows_ is zero, the position of the cursor will usually be at the bottom of the table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="549d5-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="549d5-124">See also</span></span>

- [<span data-ttu-id="549d5-125">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="549d5-125">MAPI Tables</span></span>](mapi-tables.md)

