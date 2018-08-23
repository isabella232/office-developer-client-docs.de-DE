---
title: Bestimmen des Tabelleendes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f9979baf144b6106adcec416ee04439404e05d19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576344"
---
# <a name="determining-a-tables-end"></a><span data-ttu-id="e58e5-103">Bestimmen des Tabelleendes</span><span class="sxs-lookup"><span data-stu-id="e58e5-103">Determining a Table's End</span></span>

  
  
<span data-ttu-id="e58e5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e58e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e58e5-105">Ein häufiger Fehler ist, wird davon ausgegangen, dass das Ende der Tabelle erreicht wurde hat:</span><span class="sxs-lookup"><span data-stu-id="e58e5-105">A common error is to assume that the end of the table has been reached when:</span></span> 
  
- <span data-ttu-id="e58e5-106">[IMAPITable::QueryRows](imapitable-queryrows.md) wurde in einer Schleife, mit dem Ende der Schleife durch die Anzahl der Zeilen von [IMAPITable::GetRowCount](imapitable-getrowcount.md)zurückgegebene bestimmt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e58e5-106">[IMAPITable::QueryRows](imapitable-queryrows.md) has been called in a loop, with the end of the loop determined by the row count returned by [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span></span> <span data-ttu-id="e58e5-107">Anzahl die **GetRowCount** gibt stellt keine immer die genaue Anzahl der Zeilen in der Tabelle dar; Es ist eine ungefähre Anzahl.</span><span class="sxs-lookup"><span data-stu-id="e58e5-107">The count that **GetRowCount** returns does not always represent the exact number of rows in the table; it is an approximate count.</span></span> 
    
- <span data-ttu-id="e58e5-108">**QueryRows** mit einer festen Anzahl von Zeilen aufgerufen wurde, und es werden weniger Zeilen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e58e5-108">**QueryRows** has been called with a fixed number of rows and fewer rows are returned.</span></span> <span data-ttu-id="e58e5-109">Erst **QueryRows** ein Rowset mit einer Zeilenanzahl gleich 0 (null), die es keine weiteren Zeilen gibt sind abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e58e5-109">It is not until **QueryRows** returns a row set with a row count equal to zero that there are no more rows to retrieve.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="e58e5-110">Die einzige Zeit, die ein Anrufer übernehmen kann, dass sich der Cursor am Ende der Tabelle für eine positive Zeilenanzahl oder am Anfang der Tabelle eine negative Zeilenanzahl befindet ist, wenn der Wert S_OK und keine Zeilen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e58e5-110">The only time that a caller can assume that the cursor is positioned at the end of the table for a positive row count or at the beginning of the table for a negative row count is when the value S_OK and zero rows are returned.</span></span> <span data-ttu-id="e58e5-111">Der Wert wird nie MAPI_E_NOT_FOUND zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e58e5-111">The value MAPI_E_NOT_FOUND is never returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e58e5-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e58e5-112">See also</span></span>



[<span data-ttu-id="e58e5-113">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="e58e5-113">MAPI Tables</span></span>](mapi-tables.md)

