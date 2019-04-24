---
title: Recordset2. MoveLast-Methode (DAO)
TOCTitle: MoveLast Method
ms:assetid: 32717786-c59c-ec22-666b-fc78e4265c5a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192306(v=office.15)
ms:contentKeyID: 48544079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 829c4dd759bce86388cc65aa5b63276eec438ea0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307259"
---
# <a name="recordset2movelast-method-dao"></a><span data-ttu-id="63c93-102">Recordset2. MoveLast-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="63c93-102">Recordset2.MoveLast method (DAO)</span></span>

<span data-ttu-id="63c93-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63c93-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63c93-104">Wechselt zum letzten Datensatz in einem angegebenen **Recordset**-Objekt und macht diesen zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="63c93-104">Moves to the last record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="63c93-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="63c93-105">Syntax</span></span>

<span data-ttu-id="63c93-106">*Ausdruck* . MoveLast (***Optionen***)</span><span class="sxs-lookup"><span data-stu-id="63c93-106">*expression* .MoveLast(***Options***)</span></span>

<span data-ttu-id="63c93-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="63c93-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="63c93-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="63c93-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="63c93-109">Name</span><span class="sxs-lookup"><span data-stu-id="63c93-109">Name</span></span></p></th>
<th><p><span data-ttu-id="63c93-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="63c93-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="63c93-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="63c93-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="63c93-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63c93-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63c93-113"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="63c93-113"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="63c93-114">Optional</span><span class="sxs-lookup"><span data-stu-id="63c93-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="63c93-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="63c93-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="63c93-116">Auf <strong>dbRunAsync</strong> festgelegt, damit der Aufruf für <strong>MoveLast</strong> asynchron ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63c93-116">Set to <strong>dbRunAsync</strong> to rune the call to <strong>MoveLast</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="63c93-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63c93-117">Remarks</span></span>

<span data-ttu-id="63c93-118">Verwenden Sie die **Move**-Methoden, um von einem Datensatz zum nächsten zu wechseln, ohne eine Bedingung anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="63c93-118">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="63c93-p101">Wenn Sie den aktuellen Datensatz bearbeiten, sollten Sie die Änderungen mit der **Update**-Methode speichern, bevor Sie zu einem anderen Datensatz wechseln. Ohne diese Aktualisierung gehen die Änderungen beim Wechseln zwischen Datensätzen ohne Warnung verloren.</span><span class="sxs-lookup"><span data-stu-id="63c93-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="63c93-p102">Beim Öffnen eines **Recordset**-Objekts ist der erste Datensatz aktuell, und die **BOF**-Eigenschaft ist auf **False** festgelegt. Wenn **Recordset** keine Datensätze enthält, ist die **BOF**-Eigenschaft auf **True** festgelegt, und es ist kein aktueller Datensatz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="63c93-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="63c93-123">Ist der erste bzw. letzte Datensatz beim Verwenden von **MoveFirst** oder **MoveLast** bereits aktuell, ändert sich der aktuelle Datensatz nicht.</span><span class="sxs-lookup"><span data-stu-id="63c93-123">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="63c93-124">Wenn Recordset auf ein **Recordset** vom Typ "Tabelle" verweist (nur Microsoft Access-Arbeitsbereiche), folgt die Bewegung dem aktuellen Index.</span><span class="sxs-lookup"><span data-stu-id="63c93-124">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="63c93-125">You can set the current index by using the **Index** property.</span><span class="sxs-lookup"><span data-stu-id="63c93-125">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="63c93-126">If you don't set the current index, the order of returned records is undefined.</span><span class="sxs-lookup"><span data-stu-id="63c93-126">If you don't set the current index, the order of returned records is undefined.</span></span>

> [!NOTE]
> <span data-ttu-id="63c93-127">You can use the **MoveLast** method to fully populate a dynaset- or snapshot-type **Recordset** to provide the current number of records in the **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="63c93-127">You can use the **MoveLast** method to fully populate a dynaset- or snapshot-type **Recordset** to provide the current number of records in the **Recordset**.</span></span> <span data-ttu-id="63c93-128">However, if you use **MoveLast** in this way, you can slow down your application's performance.</span><span class="sxs-lookup"><span data-stu-id="63c93-128">However, if you use **MoveLast** in this way, you can slow down your application's performance.</span></span> <span data-ttu-id="63c93-129">You should only use **MoveLast** to get a record count if it is absolutely necessary to obtain an accurate record count on a newly opened **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="63c93-129">You should only use **MoveLast** to get a record count if it is absolutely necessary to obtain an accurate record count on a newly opened **Recordset**.</span></span> 
>
> <span data-ttu-id="63c93-130">If you use the **dbRunAsync** constant with **MoveLast**, the method call is asynchronous.</span><span class="sxs-lookup"><span data-stu-id="63c93-130">If you use the **dbRunAsync** constant with **MoveLast**, the method call is asynchronous.</span></span> <span data-ttu-id="63c93-131">You can use the **StillExecuting** property to determine when the **Recordset** is fully populated, and you can use the **Cancel** method to terminate execution of the asynchronous **MoveLast** method call.</span><span class="sxs-lookup"><span data-stu-id="63c93-131">You can use the **StillExecuting** property to determine when the **Recordset** is fully populated, and you can use the **Cancel** method to terminate execution of the asynchronous **MoveLast** method call.</span></span>

<span data-ttu-id="63c93-132">Die Methoden **MoveFirst**, **MoveLast** und **MovePrevious** können für ein **Recordset**-Objekt vom Typ "Forward-only" nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63c93-132">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="63c93-133">Um die Position des aktuellen Datensatzes in einem **Recordset**-Objekt um eine bestimmte Anzahl von Datensätzen nach vorne oder hinten zu verschieben, verwenden Sie die **Move**-Methode.</span><span class="sxs-lookup"><span data-stu-id="63c93-133">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

