---
title: Informationen zum asynchronen Tabellenvorgänge
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1c31045e1fc19da63a2d4b61d92b3629afc96a55
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569421"
---
# <a name="about-asynchronous-table-operations"></a><span data-ttu-id="199f6-103">Informationen zum asynchronen Tabellenvorgänge</span><span class="sxs-lookup"><span data-stu-id="199f6-103">About asynchronous table operations</span></span>
 
<span data-ttu-id="199f6-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="199f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="199f6-105">Die **IMAPITable** -Schnittstelle umfasst drei Methoden, die asynchron arbeiten und drei Methoden zum Steuern einer asynchronen Operation.</span><span class="sxs-lookup"><span data-stu-id="199f6-105">The **IMAPITable** interface includes three methods that operate asynchronously and three methods for controlling an asynchronous operation.</span></span> <span data-ttu-id="199f6-106">Die folgende Tabelle enthält die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="199f6-106">The following table lists these methods:</span></span> 
  
|<span data-ttu-id="199f6-107">**Asynchrone operation**</span><span class="sxs-lookup"><span data-stu-id="199f6-107">**Asynchronous operation**</span></span>|<span data-ttu-id="199f6-108">**Asynchrone Steuerelementmethode**</span><span class="sxs-lookup"><span data-stu-id="199f6-108">**Asynchronous control method**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="199f6-109">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="199f6-109">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |[<span data-ttu-id="199f6-110">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="199f6-110">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md) <br/> |
|[<span data-ttu-id="199f6-111">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="199f6-111">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |[<span data-ttu-id="199f6-112">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="199f6-112">IMAPITable::Abort</span></span>](imapitable-abort.md) <br/> |
|[<span data-ttu-id="199f6-113">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="199f6-113">IMAPITable::SortTable</span></span>](imapitable-sorttable.md) <br/> |[<span data-ttu-id="199f6-114">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="199f6-114">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |
   
<span data-ttu-id="199f6-115">**Zum Abrufen von Statusinformationen über den Typ und die aktuelle Vorgang einer Tabelle**</span><span class="sxs-lookup"><span data-stu-id="199f6-115">**To retrieve status information about a table's type and current operation**</span></span>
  
- <span data-ttu-id="199f6-116">Rufen Sie [IMAPITable::GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="199f6-116">Call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span> <span data-ttu-id="199f6-117">Bei **GetStatus**kann ein Tabelle Benutzer bestimmen, gibt an, ob die Tabelle statische oder dynamische, ist, wenn ein Vorgang noch in Arbeit ist oder abgeschlossen ist, und wenn aus einer abgeschlossenen Vorgangs ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="199f6-117">With **GetStatus**, a table user can determine whether the table is static or dynamic, if an operation is in progress or has completed, and if an error has occurred from a completed operation.</span></span> <span data-ttu-id="199f6-118">Beispielsweise wenn ein Client muss einen Sortiervorgang abzubrechen, da es zu lange dauert, kann der Client zunächst Aufrufen **GetStatus** , um festzustellen, ob tatsächlich ein Sortiervorgang zurzeit verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="199f6-118">For example, if a client needs to cancel a sort operation because it is taking too much time, the client can first call **GetStatus** to determine whether, in fact, a sort operation is presently processing.</span></span> <span data-ttu-id="199f6-119">Der Client kann dann [IMAPITable::Abort](imapitable-abort.md) unterbrochen werden, um aufrufen.</span><span class="sxs-lookup"><span data-stu-id="199f6-119">Then the client can call [IMAPITable::Abort](imapitable-abort.md) to stop it.</span></span> 
    
<span data-ttu-id="199f6-120">**Um Aktivität anzuhalten, bis eine asynchrone Aufgabe abgeschlossen wurde**</span><span class="sxs-lookup"><span data-stu-id="199f6-120">**To suspend activity until an asynchronous task has completed**</span></span>
  
- <span data-ttu-id="199f6-121">Rufen Sie [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span><span class="sxs-lookup"><span data-stu-id="199f6-121">Call [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span></span> <span data-ttu-id="199f6-122">Aufrufen von **WaitForCompletion** ermöglicht die Aufgabe ohne Unterbrechung abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="199f6-122">Calling **WaitForCompletion** allows the task to complete without interruption.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="199f6-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="199f6-123">See also</span></span>

- [<span data-ttu-id="199f6-124">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="199f6-124">MAPI Tables</span></span>](mapi-tables.md)

