---
title: Recordset.MoveLast-Methode (DAO)
TOCTitle: MoveLast Method
ms:assetid: fc0f7a33-1f55-9f5b-b00d-1b81f49b1c3e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837192(v=office.15)
ms:contentKeyID: 48548881
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44b38825ad2757be1cb17bfc7f7a6721bc073968
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920095"
---
# <a name="recordsetmovelast-method-dao"></a><span data-ttu-id="8d340-102">Recordset.MoveLast-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="8d340-102">Recordset.MoveLast method (DAO)</span></span>


<span data-ttu-id="8d340-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d340-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d340-104">Wechselt zum letzten Datensatz in einem angegebenen **Recordset**-Objekt und macht diesen zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="8d340-104">Moves to the last record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d340-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d340-105">Syntax</span></span>

<span data-ttu-id="8d340-106">*Ausdruck* . MoveLast (***Optionen***)</span><span class="sxs-lookup"><span data-stu-id="8d340-106">*expression* .MoveLast(***Options***)</span></span>

<span data-ttu-id="8d340-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8d340-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="8d340-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d340-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d340-109">Name</span><span class="sxs-lookup"><span data-stu-id="8d340-109">Name</span></span></p></th>
<th><p><span data-ttu-id="8d340-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="8d340-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="8d340-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8d340-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="8d340-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d340-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d340-113">Optionen</span><span class="sxs-lookup"><span data-stu-id="8d340-113">Options</span></span></p></td>
<td><p><span data-ttu-id="8d340-114">Optional</span><span class="sxs-lookup"><span data-stu-id="8d340-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="8d340-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="8d340-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="8d340-116">Auf <strong>dbRunAsync</strong> festgelegt, damit der Aufruf für <strong>MoveLast</strong> asynchron ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d340-116">Set to <strong>dbRunAsync</strong> to rune the call to <strong>MoveLast</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8d340-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d340-117">Remarks</span></span>

<span data-ttu-id="8d340-118">Verwenden Sie die **Move**-Methoden, um von einem Datensatz zum nächsten zu wechseln, ohne eine Bedingung anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="8d340-118">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="8d340-p101">Wenn Sie den aktuellen Datensatz bearbeiten, sollten Sie die Änderungen mit der **Update**-Methode speichern, bevor Sie zu einem anderen Datensatz wechseln. Ohne diese Aktualisierung gehen die Änderungen beim Wechseln zwischen Datensätzen ohne Warnung verloren.</span><span class="sxs-lookup"><span data-stu-id="8d340-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="8d340-p102">Beim Öffnen eines **Recordset**-Objekts ist der erste Datensatz aktuell, und die **BOF**-Eigenschaft ist auf **False** festgelegt. Wenn **Recordset** keine Datensätze enthält, ist die **BOF**-Eigenschaft auf **True** festgelegt, und es ist kein aktueller Datensatz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8d340-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="8d340-123">Ist der erste bzw. letzte Datensatz beim Verwenden von **MoveFirst** oder **MoveLast** bereits aktuell, ändert sich der aktuelle Datensatz nicht.</span><span class="sxs-lookup"><span data-stu-id="8d340-123">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="8d340-124">Wenn Recordset vom Typ Tabelle **Recordset-Objekt** (nur Microsoft Access-Arbeitsbereiche) bezieht, folgt die Verschiebung den aktuellen Index.</span><span class="sxs-lookup"><span data-stu-id="8d340-124">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="8d340-125">Sie können den aktuellen Index mit der **Index** -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="8d340-125">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="8d340-126">Wenn Sie den aktuellen Index nicht festlegen, ist die Reihenfolge der zurückgegebenen Datensätze nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="8d340-126">If you don't set the current index, the order of returned records is undefined.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8d340-p104">Mithilfe der MoveLast-Methode können Sie ein Recordset vom Typ Dynaset oder Snapshot vollständig auffüllen, um die aktuelle Anzahl von Datensätzen im Recordset anzugeben. Wenn Sie allerdings MoveLast auf diese Weise verwenden, kann dies die Leistung der Anwendung beeinträchtigen. Sie sollten nur dann mithilfe von MoveLast eine Datensatzanzahl abrufen, wenn Sie unbedingt eine genaue Anzahl für ein neu geöffnetes Recordset benötigen. Wenn Sie die dbRunAsync-Konstante mit MoveLast verwenden, ist der Methodenaufruf asynchron. Sie können die StillExecuting-Eigenschaft verwenden, um festzustellen, ob das Recordset vollständig aufgefüllt ist. Mit der Cancel-Methode beenden Sie die Ausführung des asynchronen MoveLast-Methodenaufrufs.</span><span class="sxs-lookup"><span data-stu-id="8d340-p104">You can use the <STRONG>MoveLast</STRONG> method to fully populate a dynaset- or snapshot-type <STRONG>Recordset</STRONG> to provide the current number of records in the <STRONG>Recordset</STRONG>. However, if you use <STRONG>MoveLast</STRONG> in this way, you can slow down your application's performance. You should only use <STRONG>MoveLast</STRONG> to get a record count if it is absolutely necessary to obtain an accurate record count on a newly opened <STRONG>Recordset</STRONG>. If you use the <STRONG>dbRunAsync</STRONG> constant with <STRONG>MoveLast</STRONG>, the method call is asynchronous. You can use the <STRONG>StillExecuting</STRONG> property to determine when the <STRONG>Recordset</STRONG> is fully populated, and you can use the <STRONG>Cancel</STRONG> method to terminate execution of the asynchronous <STRONG>MoveLast</STRONG> method call.</span></span></P>



<span data-ttu-id="8d340-132">Sie können nicht auf ein **Recordset** -Objekt weiterleiten – nur – Geben Sie die **MoveFirst**, **MoveLast**und **MovePrevious** -Methoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d340-132">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="8d340-133">Verwenden Sie die **Move**-Methode, um die Position des aktuellen Datensatzes in einem **Recordset**-Objekt um eine bestimmte Anzahl von Datensätzen vorwärts oder rückwärts zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="8d340-133">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

