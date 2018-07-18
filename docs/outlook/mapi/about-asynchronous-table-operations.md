---
title: Informationen zum asynchronen Tabellenvorgänge
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 99bff153d4ce4bac3f85e0ed0feeaffafa6bf3f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791218"
---
# <a name="about-asynchronous-table-operations"></a><span data-ttu-id="2b76a-103">Informationen zum asynchronen Tabellenvorgänge</span><span class="sxs-lookup"><span data-stu-id="2b76a-103">About asynchronous table operations</span></span>
 
<span data-ttu-id="2b76a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2b76a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2b76a-105">Die **IMAPITable** -Schnittstelle umfasst drei Methoden, die asynchron arbeiten und drei Methoden zum Steuern einer asynchronen Operation.</span><span class="sxs-lookup"><span data-stu-id="2b76a-105">The **IMAPITable** interface includes three methods that operate asynchronously and three methods for controlling an asynchronous operation.</span></span> <span data-ttu-id="2b76a-106">Die folgende Tabelle enthält die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="2b76a-106">The following table lists these methods:</span></span> 
  
|<span data-ttu-id="2b76a-107">**Asynchrone operation**</span><span class="sxs-lookup"><span data-stu-id="2b76a-107">**Asynchronous operation**</span></span>|<span data-ttu-id="2b76a-108">**Asynchrone Steuerelementmethode**</span><span class="sxs-lookup"><span data-stu-id="2b76a-108">**Asynchronous control method**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b76a-109">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="2b76a-109">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |[<span data-ttu-id="2b76a-110">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="2b76a-110">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md) <br/> |
|[<span data-ttu-id="2b76a-111">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="2b76a-111">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |[<span data-ttu-id="2b76a-112">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="2b76a-112">IMAPITable::Abort</span></span>](imapitable-abort.md) <br/> |
|[<span data-ttu-id="2b76a-113">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="2b76a-113">IMAPITable::SortTable</span></span>](imapitable-sorttable.md) <br/> |[<span data-ttu-id="2b76a-114">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="2b76a-114">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |
   
<span data-ttu-id="2b76a-115">**Zum Abrufen von Statusinformationen über den Typ und die aktuelle Vorgang einer Tabelle**</span><span class="sxs-lookup"><span data-stu-id="2b76a-115">**To retrieve status information about a table's type and current operation**</span></span>
  
- <span data-ttu-id="2b76a-116">Rufen Sie [IMAPITable::GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="2b76a-116">Call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span> <span data-ttu-id="2b76a-117">Bei **GetStatus**kann ein Tabelle Benutzer bestimmen, gibt an, ob die Tabelle statische oder dynamische, ist, wenn ein Vorgang noch in Arbeit ist oder abgeschlossen ist, und wenn aus einer abgeschlossenen Vorgangs ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2b76a-117">With **GetStatus**, a table user can determine whether the table is static or dynamic, if an operation is in progress or has completed, and if an error has occurred from a completed operation.</span></span> <span data-ttu-id="2b76a-118">Beispielsweise wenn ein Client muss einen Sortiervorgang abzubrechen, da es zu lange dauert, kann der Client zunächst Aufrufen **GetStatus** , um festzustellen, ob tatsächlich ein Sortiervorgang zurzeit verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="2b76a-118">For example, if a client needs to cancel a sort operation because it is taking too much time, the client can first call **GetStatus** to determine whether, in fact, a sort operation is presently processing.</span></span> <span data-ttu-id="2b76a-119">Der Client kann dann [IMAPITable::Abort](imapitable-abort.md) unterbrochen werden, um aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2b76a-119">Then the client can call [IMAPITable::Abort](imapitable-abort.md) to stop it.</span></span> 
    
<span data-ttu-id="2b76a-120">**Um Aktivität anzuhalten, bis eine asynchrone Aufgabe abgeschlossen wurde**</span><span class="sxs-lookup"><span data-stu-id="2b76a-120">**To suspend activity until an asynchronous task has completed**</span></span>
  
- <span data-ttu-id="2b76a-121">Rufen Sie [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span><span class="sxs-lookup"><span data-stu-id="2b76a-121">Call [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span></span> <span data-ttu-id="2b76a-122">Aufrufen von **WaitForCompletion** ermöglicht die Aufgabe ohne Unterbrechung abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="2b76a-122">Calling **WaitForCompletion** allows the task to complete without interruption.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2b76a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b76a-123">See also</span></span>

- [<span data-ttu-id="2b76a-124">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="2b76a-124">MAPI Tables</span></span>](mapi-tables.md)

