---
title: Recordset2.MoveFirst-Methode (DAO)
TOCTitle: MoveFirst Method
ms:assetid: 74b186d0-8f6a-d136-a563-04f58d67b122
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195879(v=office.15)
ms:contentKeyID: 48545667
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bd5225e2fdbf662180b3cb11f48c8e7ba65b706a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921369"
---
# <a name="recordset2movefirst-method-dao"></a><span data-ttu-id="54fe8-102">Recordset2.MoveFirst-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="54fe8-102">Recordset2.MoveFirst method (DAO)</span></span>


<span data-ttu-id="54fe8-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="54fe8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="54fe8-104">Wechselt zum ersten Datensatz in einem angegebenen **Recordset**-Objekt und macht diesen zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="54fe8-104">Moves to the first record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="54fe8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54fe8-105">Syntax</span></span>

<span data-ttu-id="54fe8-106">*Ausdruck* . MoveFirst</span><span class="sxs-lookup"><span data-stu-id="54fe8-106">*expression* .MoveFirst</span></span>

<span data-ttu-id="54fe8-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="54fe8-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="54fe8-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="54fe8-108">Remarks</span></span>

<span data-ttu-id="54fe8-109">Verwenden Sie die **Move**-Methoden, um von einem Datensatz zum nächsten zu wechseln, ohne eine Bedingung anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="54fe8-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="54fe8-p101">Wenn Sie den aktuellen Datensatz bearbeiten, sollten Sie die Änderungen mit der **Update**-Methode speichern, bevor Sie zu einem anderen Datensatz wechseln. Ohne diese Aktualisierung gehen die Änderungen beim Wechseln zwischen Datensätzen ohne Warnung verloren.</span><span class="sxs-lookup"><span data-stu-id="54fe8-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="54fe8-p102">Beim Öffnen eines **Recordset**-Objekts ist der erste Datensatz aktuell, und die **BOF**-Eigenschaft ist auf **False** festgelegt. Wenn **Recordset** keine Datensätze enthält, ist die **BOF**-Eigenschaft auf **True** festgelegt, und es ist kein aktueller Datensatz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="54fe8-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="54fe8-114">Ist der erste bzw. letzte Datensatz beim Verwenden von **MoveFirst** oder **MoveLast** bereits aktuell, ändert sich der aktuelle Datensatz nicht.</span><span class="sxs-lookup"><span data-stu-id="54fe8-114">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="54fe8-115">Wenn Recordset vom Typ Tabelle **Recordset-Objekt** (nur Microsoft Access-Arbeitsbereiche) bezieht, folgt die Verschiebung den aktuellen Index.</span><span class="sxs-lookup"><span data-stu-id="54fe8-115">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="54fe8-116">Sie können den aktuellen Index mit der **Index** -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="54fe8-116">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="54fe8-117">Wenn Sie den aktuellen Index nicht festlegen, ist die Reihenfolge der zurückgegebenen Datensätze nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="54fe8-117">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="54fe8-118">Sie können nicht auf ein **Recordset** -Objekt weiterleiten – nur – Geben Sie die **MoveFirst**, **MoveLast**und **MovePrevious** -Methoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="54fe8-118">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="54fe8-119">Verwenden Sie die **Move**-Methode, um die Position des aktuellen Datensatzes in einem **Recordset**-Objekt um eine bestimmte Anzahl von Datensätzen vorwärts oder rückwärts zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="54fe8-119">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

