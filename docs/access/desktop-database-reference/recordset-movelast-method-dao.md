---
title: Recordset.MoveLast-Methode (DAO)
TOCTitle: MoveLast method
ms:assetid: fc0f7a33-1f55-9f5b-b00d-1b81f49b1c3e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837192(v=office.15)
ms:contentKeyID: 48548881
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 79799742499e163a43d51a2d8553adcadf27b36d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715270"
---
# <a name="recordsetmovelast-method-dao"></a><span data-ttu-id="80840-102">Recordset.MoveLast-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="80840-102">Recordset.MoveLast method (DAO)</span></span>

<span data-ttu-id="80840-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="80840-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="80840-104">Wechselt zum letzten Datensatz in einem angegebenen **Recordset**-Objekt und macht diesen zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="80840-104">Moves to the last record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="80840-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="80840-105">Syntax</span></span>

<span data-ttu-id="80840-106">*Ausdruck* . MoveLast (***Optionen***)</span><span class="sxs-lookup"><span data-stu-id="80840-106">*expression* .MoveLast(***Options***)</span></span>

<span data-ttu-id="80840-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="80840-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="80840-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="80840-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="80840-109">Name</span><span class="sxs-lookup"><span data-stu-id="80840-109">Name</span></span></p></th>
<th><p><span data-ttu-id="80840-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="80840-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="80840-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="80840-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="80840-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80840-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80840-113"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="80840-113"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="80840-114">Optional</span><span class="sxs-lookup"><span data-stu-id="80840-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="80840-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="80840-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="80840-116">Auf <strong>dbRunAsync</strong> festgelegt, damit der Aufruf für <strong>MoveLast</strong> asynchron ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80840-116">Set to <strong>dbRunAsync</strong> to rune the call to <strong>MoveLast</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="80840-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80840-117">Remarks</span></span>

<span data-ttu-id="80840-118">Verwenden Sie die **Move**-Methoden, um von einem Datensatz zum nächsten zu wechseln, ohne eine Bedingung anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="80840-118">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="80840-p101">Wenn Sie den aktuellen Datensatz bearbeiten, sollten Sie die Änderungen mit der **Update**-Methode speichern, bevor Sie zu einem anderen Datensatz wechseln. Ohne diese Aktualisierung gehen die Änderungen beim Wechseln zwischen Datensätzen ohne Warnung verloren.</span><span class="sxs-lookup"><span data-stu-id="80840-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="80840-p102">Beim Öffnen eines **Recordset**-Objekts ist der erste Datensatz aktuell, und die **BOF**-Eigenschaft ist auf **False** festgelegt. Wenn **Recordset** keine Datensätze enthält, ist die **BOF**-Eigenschaft auf **True** festgelegt, und es ist kein aktueller Datensatz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="80840-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="80840-123">Ist der erste bzw. letzte Datensatz beim Verwenden von **MoveFirst** oder **MoveLast** bereits aktuell, ändert sich der aktuelle Datensatz nicht.</span><span class="sxs-lookup"><span data-stu-id="80840-123">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="80840-124">Wenn Recordset vom Typ Tabelle **Recordset-Objekt** (nur Microsoft Access-Arbeitsbereiche) bezieht, folgt die Verschiebung den aktuellen Index.</span><span class="sxs-lookup"><span data-stu-id="80840-124">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="80840-125">Sie können den aktuellen Index mit der **Index** -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="80840-125">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="80840-126">Wenn Sie den aktuellen Index nicht festlegen, ist die Reihenfolge der zurückgegebenen Datensätze nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="80840-126">If you don't set the current index, the order of returned records is undefined.</span></span>

> [!NOTE]
> <span data-ttu-id="80840-127">Die **MoveLast** -Methode können Sie vollständig auffüllen einen Typ Dynaset oder Snapshot- **Recordset-Objekts** , um die aktuelle Anzahl der Datensätze im **Recordset-Objekt**enthalten.</span><span class="sxs-lookup"><span data-stu-id="80840-127">You can use the **MoveLast** method to fully populate a dynaset- or snapshot-type **Recordset** to provide the current number of records in the **Recordset**.</span></span> <span data-ttu-id="80840-128">Jedoch, wenn Sie auf diese Weise **MoveLast** verwenden, können Sie die Leistung der Anwendung verlangsamen.</span><span class="sxs-lookup"><span data-stu-id="80840-128">However, if you use **MoveLast** in this way, you can slow down your application's performance.</span></span> <span data-ttu-id="80840-129">Sie sollten nur **MoveLast** verwenden, um zählen der Datensätze abzurufen, wenn dies unbedingt erforderlich ist, erhalten Sie eine genaue Anzahl für ein neu geöffneten **Recordset-Objekt**ist.</span><span class="sxs-lookup"><span data-stu-id="80840-129">You should only use **MoveLast** to get a record count if it is absolutely necessary to obtain an accurate record count on a newly opened **Recordset**.</span></span> 
> 
> <span data-ttu-id="80840-130">Wenn Sie die Konstante **DbRunAsync** mit **MoveLast**verwenden, ist der Methodenaufruf asynchron.</span><span class="sxs-lookup"><span data-stu-id="80840-130">If you use the **dbRunAsync** constant with **MoveLast**, the method call is asynchronous.</span></span> <span data-ttu-id="80840-131">Die **StillExecuting** -Eigenschaft können Sie bestimmen, wann **Recordset** vollständig aufgefüllt wird, und Sie können die **Cancel** -Methode verwenden, um die Ausführung des asynchronen Aufrufs **MoveLast** -Methode beendet werden.</span><span class="sxs-lookup"><span data-stu-id="80840-131">You can use the **StillExecuting** property to determine when the **Recordset** is fully populated, and you can use the **Cancel** method to terminate execution of the asynchronous **MoveLast** method call.</span></span>

<span data-ttu-id="80840-132">Sie können nicht auf ein **Recordset** -Objekt weiterleiten – nur – Geben Sie die **MoveFirst**, **MoveLast**und **MovePrevious** -Methoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="80840-132">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="80840-133">Verwenden Sie die **Move**-Methode, um die Position des aktuellen Datensatzes in einem **Recordset**-Objekt um eine bestimmte Anzahl von Datensätzen vorwärts oder rückwärts zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="80840-133">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

