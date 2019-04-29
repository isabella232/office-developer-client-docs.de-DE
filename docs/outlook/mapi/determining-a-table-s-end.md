---
title: Bestimmen des Endes einer Tabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 28892e2d351b8dc9aa864c9eff52c94bb0f20e8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420087"
---
# <a name="determining-a-tables-end"></a><span data-ttu-id="8da64-103">Bestimmen des Endes einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="8da64-103">Determining a Table's End</span></span>

  
  
<span data-ttu-id="8da64-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8da64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="8da64-105">Eine häufige Fehlermeldung ist, dass das Ende der Tabelle erreicht wurde, wenn:</span><span class="sxs-lookup"><span data-stu-id="8da64-105">A common error is to assume that the end of the table has been reached when:</span></span> 
  
- <span data-ttu-id="8da64-106">[IMAPITable:: QueryRows](imapitable-queryrows.md) wurde in einer Schleife aufgerufen, wobei das Ende der Schleife durch die von [IMAPITable:: GetRowCount](imapitable-getrowcount.md)zurückgegebene Zeilenanzahl bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="8da64-106">[IMAPITable::QueryRows](imapitable-queryrows.md) has been called in a loop, with the end of the loop determined by the row count returned by [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span></span> <span data-ttu-id="8da64-107">Die von **GetRowCount** zurückgegebene Anzahl stellt nicht immer die genaue Anzahl der Zeilen in der Tabelle dar. Es handelt sich um eine ungefähre Anzahl.</span><span class="sxs-lookup"><span data-stu-id="8da64-107">The count that **GetRowCount** returns does not always represent the exact number of rows in the table; it is an approximate count.</span></span> 
    
- <span data-ttu-id="8da64-108">**QueryRows** wurde mit einer festen Anzahl von Zeilen aufgerufen, und es werden weniger Zeilen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8da64-108">**QueryRows** has been called with a fixed number of rows and fewer rows are returned.</span></span> <span data-ttu-id="8da64-109">Erst wenn **QueryRows** einen Zeilensatz mit einer Zeilenanzahl gleich 0 (null) zurückgibt, dass keine weiteren Zeilen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8da64-109">It is not until **QueryRows** returns a row set with a row count equal to zero that there are no more rows to retrieve.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="8da64-110">Ein Anrufer kann nur davon ausgehen, dass der Cursor am Ende der Tabelle für eine positive Zeilenanzahl oder am Anfang der Tabelle für eine negative Zeilenanzahl positioniert ist, wenn der Wert S_OK und null Zeilen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8da64-110">The only time that a caller can assume that the cursor is positioned at the end of the table for a positive row count or at the beginning of the table for a negative row count is when the value S_OK and zero rows are returned.</span></span> <span data-ttu-id="8da64-111">Der Wert MAPI_E_NOT_FOUND wird nie zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8da64-111">The value MAPI_E_NOT_FOUND is never returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8da64-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8da64-112">See also</span></span>



[<span data-ttu-id="8da64-113">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="8da64-113">MAPI Tables</span></span>](mapi-tables.md)

