---
title: Recordset2.MoveLast-Methode (DAO)
TOCTitle: MoveLast Method
ms:assetid: 32717786-c59c-ec22-666b-fc78e4265c5a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192306(v=office.15)
ms:contentKeyID: 48544079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 83db6ae8da804237222fc1f58e03058951d7ce41
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998987"
---
# <a name="recordset2movelast-method-dao"></a><span data-ttu-id="cfa29-102">Recordset2.MoveLast-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="cfa29-102">Recordset2.MoveLast method (DAO)</span></span>

<span data-ttu-id="cfa29-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cfa29-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cfa29-104">Wechselt zum letzten Datensatz in einem angegebenen **Recordset**-Objekt und macht diesen zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="cfa29-104">Moves to the last record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfa29-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfa29-105">Syntax</span></span>

<span data-ttu-id="cfa29-106">*Ausdruck* . MoveLast (***Optionen***)</span><span class="sxs-lookup"><span data-stu-id="cfa29-106">*expression* .MoveLast(***Options***)</span></span>

<span data-ttu-id="cfa29-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="cfa29-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfa29-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfa29-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cfa29-109">Name</span><span class="sxs-lookup"><span data-stu-id="cfa29-109">Name</span></span></p></th>
<th><p><span data-ttu-id="cfa29-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="cfa29-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="cfa29-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="cfa29-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="cfa29-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cfa29-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cfa29-113"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="cfa29-113"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="cfa29-114">Optional</span><span class="sxs-lookup"><span data-stu-id="cfa29-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="cfa29-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="cfa29-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="cfa29-116">Auf <strong>dbRunAsync</strong> festgelegt, damit der Aufruf für <strong>MoveLast</strong> asynchron ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cfa29-116">Set to <strong>dbRunAsync</strong> to rune the call to <strong>MoveLast</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="cfa29-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cfa29-117">Remarks</span></span>

<span data-ttu-id="cfa29-118">Verwenden Sie die **Move**-Methoden, um von einem Datensatz zum nächsten zu wechseln, ohne eine Bedingung anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="cfa29-118">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="cfa29-p101">Wenn Sie den aktuellen Datensatz bearbeiten, sollten Sie die Änderungen mit der **Update**-Methode speichern, bevor Sie zu einem anderen Datensatz wechseln. Ohne diese Aktualisierung gehen die Änderungen beim Wechseln zwischen Datensätzen ohne Warnung verloren.</span><span class="sxs-lookup"><span data-stu-id="cfa29-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="cfa29-p102">Beim Öffnen eines **Recordset**-Objekts ist der erste Datensatz aktuell, und die **BOF**-Eigenschaft ist auf **False** festgelegt. Wenn **Recordset** keine Datensätze enthält, ist die **BOF**-Eigenschaft auf **True** festgelegt, und es ist kein aktueller Datensatz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cfa29-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="cfa29-123">Ist der erste bzw. letzte Datensatz beim Verwenden von **MoveFirst** oder **MoveLast** bereits aktuell, ändert sich der aktuelle Datensatz nicht.</span><span class="sxs-lookup"><span data-stu-id="cfa29-123">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="cfa29-124">Wenn Recordset vom Typ Tabelle **Recordset-Objekt** (nur Microsoft Access-Arbeitsbereiche) bezieht, folgt die Verschiebung den aktuellen Index.</span><span class="sxs-lookup"><span data-stu-id="cfa29-124">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="cfa29-125">Sie können den aktuellen Index mit der **Index** -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="cfa29-125">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="cfa29-126">Wenn Sie den aktuellen Index nicht festlegen, ist die Reihenfolge der zurückgegebenen Datensätze nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="cfa29-126">If you don't set the current index, the order of returned records is undefined.</span></span>

> [!NOTE]
> <span data-ttu-id="cfa29-127">Die **MoveLast** -Methode können Sie vollständig auffüllen einen Typ Dynaset oder Snapshot- **Recordset-Objekts** , um die aktuelle Anzahl der Datensätze im **Recordset-Objekt**enthalten.</span><span class="sxs-lookup"><span data-stu-id="cfa29-127">You can use the **MoveLast** method to fully populate a dynaset- or snapshot-type **Recordset** to provide the current number of records in the **Recordset**.</span></span> <span data-ttu-id="cfa29-128">Jedoch, wenn Sie auf diese Weise **MoveLast** verwenden, können Sie die Leistung der Anwendung verlangsamen.</span><span class="sxs-lookup"><span data-stu-id="cfa29-128">However, if you use **MoveLast** in this way, you can slow down your application's performance.</span></span> <span data-ttu-id="cfa29-129">Sie sollten nur **MoveLast** verwenden, um zählen der Datensätze abzurufen, wenn dies unbedingt erforderlich ist, erhalten Sie eine genaue Anzahl für ein neu geöffneten **Recordset-Objekt**ist.</span><span class="sxs-lookup"><span data-stu-id="cfa29-129">You should only use **MoveLast** to get a record count if it is absolutely necessary to obtain an accurate record count on a newly opened **Recordset**.</span></span> 
>
> <span data-ttu-id="cfa29-130">Wenn Sie die Konstante **DbRunAsync** mit **MoveLast**verwenden, ist der Methodenaufruf asynchron.</span><span class="sxs-lookup"><span data-stu-id="cfa29-130">If you use the **dbRunAsync** constant with **MoveLast**, the method call is asynchronous.</span></span> <span data-ttu-id="cfa29-131">Die **StillExecuting** -Eigenschaft können Sie bestimmen, wann **Recordset** vollständig aufgefüllt wird, und Sie können die **Cancel** -Methode verwenden, um die Ausführung des asynchronen Aufrufs **MoveLast** -Methode beendet werden.</span><span class="sxs-lookup"><span data-stu-id="cfa29-131">You can use the **StillExecuting** property to determine when the **Recordset** is fully populated, and you can use the **Cancel** method to terminate execution of the asynchronous **MoveLast** method call.</span></span>

<span data-ttu-id="cfa29-132">Sie können nicht auf ein **Recordset** -Objekt weiterleiten – nur – Geben Sie die **MoveFirst**, **MoveLast**und **MovePrevious** -Methoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="cfa29-132">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="cfa29-133">Verwenden Sie die **Move**-Methode, um die Position des aktuellen Datensatzes in einem **Recordset**-Objekt um eine bestimmte Anzahl von Datensätzen vorwärts oder rückwärts zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="cfa29-133">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

