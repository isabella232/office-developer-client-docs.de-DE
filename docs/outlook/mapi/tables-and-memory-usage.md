---
title: Tabellen und Speicherverwendung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 390cec0cc59f189f83af2c5339512d82e125771e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795718"
---
# <a name="tables-and-memory-usage"></a><span data-ttu-id="20f11-103">Tabellen und Speicherverwendung</span><span class="sxs-lookup"><span data-stu-id="20f11-103">Tables and memory usage</span></span>

<span data-ttu-id="20f11-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="20f11-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="20f11-105">Ein wichtiger Aspekt beim Abrufen von Daten aus einer Tabelle verbunden ist, die Speicherverwendung.</span><span class="sxs-lookup"><span data-stu-id="20f11-105">An important issue connected with retrieving data from a table is memory usage.</span></span> <span data-ttu-id="20f11-106">Wenig verfügbarer Arbeitsspeicher kann [IMAPITable::QueryRows](imapitable-queryrows.md) und [HrQueryAllRows](hrqueryallrows.md) ein Fehler auftritt, kleiner als die gewünschte Anzahl von Zeilen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="20f11-106">Lack of available memory can cause [IMAPITable::QueryRows](imapitable-queryrows.md) and [HrQueryAllRows](hrqueryallrows.md) to fail, returning less than the desired number of rows.</span></span> <span data-ttu-id="20f11-107">Entscheiden, welche Methode oder der Funktion zum Abrufen von Tabellendaten hängt davon ab, ob die Tabelle im Arbeitsspeicher passt erwartet werden kann, und ist es nicht möglich, wenn Fehler zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="20f11-107">Deciding which method or function to use to retrieve table data depends on whether the table can be expected to fit in memory, and if it cannot, if failure is acceptable.</span></span> 
  
<span data-ttu-id="20f11-108">Da nicht immer leicht um die Menge der Daten zu ermitteln, die gleichzeitig in den Arbeitsspeicher passt, bietet MAPI einige grundlegenden Richtlinien für eine Clientanwendung oder Dienstanbieter, denen Sie folgen.</span><span class="sxs-lookup"><span data-stu-id="20f11-108">Because it is not always easy to determine the amount of data that will fit into memory at one time, MAPI provides some basic guidelines for a client application or service provider to follow.</span></span> <span data-ttu-id="20f11-109">Denken Sie daran, dass es sind immer Ausnahmen, basierend auf die bestimmte Tabelle Implementierung und wie die zugrunde liegenden Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="20f11-109">Remember that there are always exceptions, based on the particular table implementation and how the underlying data is stored.</span></span>
  
<span data-ttu-id="20f11-110">Die folgenden Richtlinien können verwendet werden, für die Speicherverwendung Tabelle ausgewertet werden soll:</span><span class="sxs-lookup"><span data-stu-id="20f11-110">The following guidelines can be used to evaluate table memory usage:</span></span>
  
- <span data-ttu-id="20f11-111">Clients, die gelegentlich Working Set Speicherverwendung im Bereich Megabyte tolerieren können und können davon werden keine Probleme, die eine ganze Tabelle in den Arbeitsspeicher gelesen haben.</span><span class="sxs-lookup"><span data-stu-id="20f11-111">Clients that can tolerate occasional working set memory usage in the megabyte range and can assume they will have no problems reading an entire table into memory.</span></span> 
    
- <span data-ttu-id="20f11-112">Einschränkungen haben einen Einfluss auf eine Tabelle Verwendung des Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="20f11-112">Restrictions have an affect on a table's usage of memory.</span></span> <span data-ttu-id="20f11-113">Eine stark eingeschränkte Tabelle mit einer umfangreichen Anzahl von Zeilen, wie etwa eine Inhaltstabelle kann in den Arbeitsspeicher angepasst wird, während eine uneingeschränkte große Tabelle in der Regel nicht erwartet.</span><span class="sxs-lookup"><span data-stu-id="20f11-113">A severely restricted table with an extensive number of rows, such as a contents table, can be expected to fit into memory while an unrestricted large table usually cannot.</span></span> 
    
- <span data-ttu-id="20f11-114">Einige der Tabellen Besitz MAPI wie Status, Profil, Messagingdiensts, Anbieter und Nachricht Store Tabellen, werden in der Regel im Arbeitsspeicher passen.</span><span class="sxs-lookup"><span data-stu-id="20f11-114">Several of the tables owned by MAPI such as the status, profile, message service, provider, and message store tables, will usually fit in memory.</span></span> <span data-ttu-id="20f11-115">Dies sind im Allgemeinen kleine Tabellen.</span><span class="sxs-lookup"><span data-stu-id="20f11-115">These are generally small tables.</span></span> <span data-ttu-id="20f11-116">Es gibt jedoch Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="20f11-116">However, there are exceptions.</span></span> <span data-ttu-id="20f11-117">Beispielsweise kann ein serverbasiertes Profilanbieter eine größere Profiltabelle generieren, die nicht angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="20f11-117">For example, a server-based profile provider might generate a larger profile table that will not be able to fit.</span></span>
    
<span data-ttu-id="20f11-118">Rufen Sie auf, um alle Zeilen aus einer Tabelle abzurufen, die in den Arbeitsspeicher ohne Probleme passt, [HrQueryAllRows](hrqueryallrows.md), wenn die maximale Anzahl von Zeilen auf 0 (null) festlegen.</span><span class="sxs-lookup"><span data-stu-id="20f11-118">To retrieve all of the rows from a table that will fit into memory with no problems, call [HrQueryAllRows](hrqueryallrows.md), setting the maximum number of rows to zero.</span></span>
  
<span data-ttu-id="20f11-119">Rufen Sie zum Abrufen aller Zeilen aus einer Tabelle, die möglicherweise nicht in den Arbeitsspeicher, ein Fehler generiert wird passt, **HrQueryAllRows** eine maximale Anzahl von Zeilen angeben.</span><span class="sxs-lookup"><span data-stu-id="20f11-119">To retrieve all of the rows from a table that might or might not fit into memory, generating an error, call **HrQueryAllRows** specifying a maximum number of rows.</span></span> <span data-ttu-id="20f11-120">Die maximale Anzahl von Zeilen sollte auf eine Zahl größer als die minimale Anzahl von Zeilen festgelegt werden, die erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="20f11-120">The maximum number of rows should be set to a number greater than the minimum number of rows that are needed.</span></span> <span data-ttu-id="20f11-121">Wenn ein Client mindestens 50 Zeilen aus einer Tabelle 300 Zeile zugreifen muss, sollte die maximale Anzahl der Zeilen auf mindestens 51 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="20f11-121">If a client must access at least 50 rows from a 300 row table, the maximum number of rows should be set to at least 51.</span></span> 
  
<span data-ttu-id="20f11-122">Rufen Sie alle Zeilen aus einer Tabelle, die möglicherweise nicht in den Speicher passen rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md) in einer Schleife mit relativ geringe Zeilenanzahl auf, wie im folgenden Codebeispiel veranschaulicht wird:</span><span class="sxs-lookup"><span data-stu-id="20f11-122">To retrieve all of the rows from a table that is not expected to fit into memory, call [IMAPITable::QueryRows](imapitable-queryrows.md) in a loop with a relatively small row count, as the following code sample illustrates:</span></span> 
  
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

<span data-ttu-id="20f11-123">Wenn diese Schleife abgeschlossen ist und alle Zeilen in der Tabelle verarbeitet wurden und _cRows_ NULL ist, werden die Position des Cursors in der Regel am unteren Rand der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="20f11-123">When this loop completes and all the rows in the table have been processed and  _cRows_ is zero, the position of the cursor will usually be at the bottom of the table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="20f11-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20f11-124">See also</span></span>

- [<span data-ttu-id="20f11-125">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="20f11-125">MAPI Tables</span></span>](mapi-tables.md)

