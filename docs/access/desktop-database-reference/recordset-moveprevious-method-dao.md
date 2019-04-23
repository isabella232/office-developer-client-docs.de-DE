---
title: Recordset. MovePrevious-Methode (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 82a3bc3e-5221-9a1a-1350-47bc6759edeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196699(v=office.15)
ms:contentKeyID: 48545984
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052872
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 95cf5daa9eac6644b17f47b09ebc749bd9ed928e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284511"
---
# <a name="recordsetmoveprevious-method-dao"></a><span data-ttu-id="57b3a-102">Recordset. MovePrevious-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="57b3a-102">Recordset.MovePrevious method (DAO)</span></span>


<span data-ttu-id="57b3a-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="57b3a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="57b3a-104">Wechselt zum vorherigen Datensatz in einem angegebenen **Recordset**-Objekt und macht diesen zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="57b3a-104">Moves to the previous record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="57b3a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="57b3a-105">Syntax</span></span>

<span data-ttu-id="57b3a-106">*Ausdruck* . MovePrevious</span><span class="sxs-lookup"><span data-stu-id="57b3a-106">*expression* .MovePrevious</span></span>

<span data-ttu-id="57b3a-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="57b3a-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="57b3a-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57b3a-108">Remarks</span></span>

<span data-ttu-id="57b3a-109">Verwenden Sie die **Move**-Methoden, um von einem Datensatz zum nächsten zu wechseln, ohne eine Bedingung anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="57b3a-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="57b3a-p101">Wenn Sie den aktuellen Datensatz bearbeiten, sollten Sie die Änderungen mit der **Update**-Methode speichern, bevor Sie zu einem anderen Datensatz wechseln. Ohne diese Aktualisierung gehen die Änderungen beim Wechseln zwischen Datensätzen ohne Warnung verloren.</span><span class="sxs-lookup"><span data-stu-id="57b3a-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="57b3a-p102">Beim Öffnen eines **Recordset**-Objekts ist der erste Datensatz aktuell, und die **BOF**-Eigenschaft ist auf **False** festgelegt. Wenn **Recordset** keine Datensätze enthält, ist die **BOF**-Eigenschaft auf **True** festgelegt, und es ist kein aktueller Datensatz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="57b3a-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="57b3a-p103">Wenn Sie **MovePrevious** verwenden, während der erste Datensatz aktuell ist, ist die **BOF**-Eigenschaft auf **True** festgelegt, und es ist kein aktueller Datensatz vorhanden. Beim erneuten Verwenden von **MovePrevious** tritt ein Fehler auf, und **BOF** bleibt auf **True** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="57b3a-p103">If you use **MovePrevious** when the first record is current, the **BOF** property is **True**, and there is no current record. If you use **MovePrevious** again, an error occurs, and **BOF** remains **True**.</span></span>

<span data-ttu-id="57b3a-116">Wenn Recordset auf ein **Recordset** vom Typ "Tabelle" verweist (nur Microsoft Access-Arbeitsbereiche), folgt die Bewegung dem aktuellen Index.</span><span class="sxs-lookup"><span data-stu-id="57b3a-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="57b3a-117">You can set the current index by using the **Index** property.</span><span class="sxs-lookup"><span data-stu-id="57b3a-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="57b3a-118">Wenn Sie den aktuellen Index nicht festlegen, ist die Reihenfolge der zurückgegebenen Datensätze nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="57b3a-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="57b3a-119">Die Methoden **MoveFirst**, **MoveLast** und **MovePrevious** können für ein **Recordset**-Objekt vom Typ "Forward-only" nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57b3a-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="57b3a-120">Um die Position des aktuellen Datensatzes in einem **Recordset**-Objekt um eine bestimmte Anzahl von Datensätzen nach vorne oder hinten zu verschieben, verwenden Sie die **Move**-Methode.</span><span class="sxs-lookup"><span data-stu-id="57b3a-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

