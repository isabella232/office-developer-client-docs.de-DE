---
title: Informationen zu asynchronen Tabellenvorgängen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: eebc04e2263b4a2037e167bd464a31d298b84664
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439569"
---
# <a name="about-asynchronous-table-operations"></a><span data-ttu-id="393ec-103">Informationen zu asynchronen Tabellenvorgängen</span><span class="sxs-lookup"><span data-stu-id="393ec-103">About asynchronous table operations</span></span>
 
<span data-ttu-id="393ec-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="393ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="393ec-105">Die **IMAPITable** -Schnittstelle umfasst drei Methoden, die asynchron ausgeführt werden, und drei Methoden zum Steuern eines asynchronen Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="393ec-105">The **IMAPITable** interface includes three methods that operate asynchronously and three methods for controlling an asynchronous operation.</span></span> <span data-ttu-id="393ec-106">In der folgenden Tabelle sind diese Methoden aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="393ec-106">The following table lists these methods:</span></span> 
  
|<span data-ttu-id="393ec-107">**Asynchroner Vorgang**</span><span class="sxs-lookup"><span data-stu-id="393ec-107">**Asynchronous operation**</span></span>|<span data-ttu-id="393ec-108">**Asynchrone Steuerelementmethode**</span><span class="sxs-lookup"><span data-stu-id="393ec-108">**Asynchronous control method**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="393ec-109">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="393ec-109">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |[<span data-ttu-id="393ec-110">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="393ec-110">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md) <br/> |
|[<span data-ttu-id="393ec-111">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="393ec-111">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |[<span data-ttu-id="393ec-112">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="393ec-112">IMAPITable::Abort</span></span>](imapitable-abort.md) <br/> |
|[<span data-ttu-id="393ec-113">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="393ec-113">IMAPITable::SortTable</span></span>](imapitable-sorttable.md) <br/> |[<span data-ttu-id="393ec-114">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="393ec-114">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |
   
<span data-ttu-id="393ec-115">**So rufen Sie Statusinformationen über den Typ einer Tabelle und den aktuellen Vorgang ab**</span><span class="sxs-lookup"><span data-stu-id="393ec-115">**To retrieve status information about a table's type and current operation**</span></span>
  
- <span data-ttu-id="393ec-116">Rufen Sie [IMAPITable:: GetStatus](imapitable-getstatus.md)auf.</span><span class="sxs-lookup"><span data-stu-id="393ec-116">Call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span> <span data-ttu-id="393ec-117">Mit **GetStatus**kann ein Tabellen Benutzer bestimmen, ob die Tabelle statisch oder dynamisch ist, ob ein Vorgang ausgeführt oder abgeschlossen wurde und ob ein Fehler aus einem abgeschlossenen Vorgang aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="393ec-117">With **GetStatus**, a table user can determine whether the table is static or dynamic, if an operation is in progress or has completed, and if an error has occurred from a completed operation.</span></span> <span data-ttu-id="393ec-118">Wenn ein Client beispielsweise einen Sortiervorgang abbrechen muss, da er zu viel Zeit in Anspruch nimmt, kann der Client zunächst **GetStatus** aufrufen, um zu bestimmen, ob tatsächlich ein Sortiervorgang derzeit verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="393ec-118">For example, if a client needs to cancel a sort operation because it is taking too much time, the client can first call **GetStatus** to determine whether, in fact, a sort operation is presently processing.</span></span> <span data-ttu-id="393ec-119">Der Client kann dann [IMAPITable:: Abort](imapitable-abort.md) aufrufen, um ihn zu beenden.</span><span class="sxs-lookup"><span data-stu-id="393ec-119">Then the client can call [IMAPITable::Abort](imapitable-abort.md) to stop it.</span></span> 
    
<span data-ttu-id="393ec-120">**So halten Sie die Aktivität an, bis eine asynchrone Aufgabe abgeschlossen ist**</span><span class="sxs-lookup"><span data-stu-id="393ec-120">**To suspend activity until an asynchronous task has completed**</span></span>
  
- <span data-ttu-id="393ec-121">Rufen Sie [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md)auf.</span><span class="sxs-lookup"><span data-stu-id="393ec-121">Call [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span></span> <span data-ttu-id="393ec-122">Durch Aufrufen von **WaitForCompletion** kann die Aufgabe ohne Unterbrechung abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="393ec-122">Calling **WaitForCompletion** allows the task to complete without interruption.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="393ec-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="393ec-123">See also</span></span>

- [<span data-ttu-id="393ec-124">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="393ec-124">MAPI Tables</span></span>](mapi-tables.md)

