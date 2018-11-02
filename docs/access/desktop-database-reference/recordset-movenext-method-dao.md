---
title: Recordset.MoveNext-Methode (DAO)
TOCTitle: MoveNext Method
ms:assetid: 0a1315cf-92f8-b8ef-1542-081e8c2d5be0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845090(v=office.15)
ms:contentKeyID: 48543142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f34085cf4b53bd94a9d9a7693cf68dd880e0a46
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922811"
---
# <a name="recordsetmovenext-method-dao"></a><span data-ttu-id="984d6-102">Recordset.MoveNext-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="984d6-102">Recordset.MoveNext method (DAO)</span></span>


<span data-ttu-id="984d6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="984d6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="984d6-104">Wechselt zum nächsten Datensatz in einem angegebenen **Recordset**-Objekt und macht diesen zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="984d6-104">Moves to the next record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="984d6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="984d6-105">Syntax</span></span>

<span data-ttu-id="984d6-106">*Ausdruck* . MoveNext</span><span class="sxs-lookup"><span data-stu-id="984d6-106">*expression* .MoveNext</span></span>

<span data-ttu-id="984d6-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="984d6-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="984d6-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="984d6-108">Remarks</span></span>

<span data-ttu-id="984d6-109">Verwenden Sie die **Move**-Methoden, um von einem Datensatz zum nächsten zu wechseln, ohne eine Bedingung anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="984d6-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="984d6-p101">Wenn Sie den aktuellen Datensatz bearbeiten, sollten Sie die Änderungen mit der **Update**-Methode speichern, bevor Sie zu einem anderen Datensatz wechseln. Ohne diese Aktualisierung gehen die Änderungen beim Wechseln zwischen Datensätzen ohne Warnung verloren.</span><span class="sxs-lookup"><span data-stu-id="984d6-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="984d6-p102">Beim Öffnen eines **Recordset**-Objekts ist der erste Datensatz aktuell, und die **BOF**-Eigenschaft ist auf **False** festgelegt. Wenn **Recordset** keine Datensätze enthält, ist die **BOF**-Eigenschaft auf **True** festgelegt, und es ist kein aktueller Datensatz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="984d6-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="984d6-p103">Wenn Sie **MoveNext** verwenden, während der letzte Datensatz aktuell ist, ist die **EOF**-Eigenschaft auf **True** festgelegt, und es ist kein aktueller Datensatz vorhanden. Beim erneuten Verwenden von **MoveNext** tritt ein Fehler auf, und **EOF** bleibt auf **True** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="984d6-p103">If you use **MoveNext** when the last record is current, the **EOF** property is **True**, and there is no current record. If you use **MoveNext** again, an error occurs, and **EOF** remains **True**.</span></span>

<span data-ttu-id="984d6-116">Wenn Recordset vom Typ Tabelle **Recordset-Objekt** (nur Microsoft Access-Arbeitsbereiche) bezieht, folgt die Verschiebung den aktuellen Index.</span><span class="sxs-lookup"><span data-stu-id="984d6-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="984d6-117">Sie können den aktuellen Index mit der **Index** -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="984d6-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="984d6-118">Wenn Sie den aktuellen Index nicht festlegen, ist die Reihenfolge der zurückgegebenen Datensätze nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="984d6-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="984d6-119">Sie können nicht auf ein **Recordset** -Objekt weiterleiten – nur – Geben Sie die **MoveFirst**, **MoveLast**und **MovePrevious** -Methoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="984d6-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="984d6-120">Verwenden Sie die **Move**-Methode, um die Position des aktuellen Datensatzes in einem **Recordset**-Objekt um eine bestimmte Anzahl von Datensätzen vorwärts oder rückwärts zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="984d6-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

