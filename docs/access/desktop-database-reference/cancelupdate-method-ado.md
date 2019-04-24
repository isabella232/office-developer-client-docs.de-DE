---
title: CancelUpdate-Methode (ADO)
TOCTitle: CancelUpdate method (ADO)
ms:assetid: 2bd4d168-ba52-7786-5046-44febeda88e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249065(v=office.15)
ms:contentKeyID: 48543938
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4585679688929532d7f50be9efc71b2830bb6587
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296626"
---
# <a name="cancelupdate-method-ado"></a><span data-ttu-id="51b32-102">CancelUpdate-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="51b32-102">CancelUpdate method (ADO)</span></span>


<span data-ttu-id="51b32-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51b32-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51b32-104">Alle an der aktuellen oder neuen Zeile eines [Recordset](recordset-object-ado.md)-Objekts oder der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts vorgenommenen Änderungen werden abgebrochen, bevor die [Update](update-method-ado.md)-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="51b32-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, before calling the [Update](update-method-ado.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="51b32-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="51b32-105">Syntax</span></span>

<span data-ttu-id="51b32-106">*Recordset*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="51b32-106">*recordset*.CancelUpdate</span></span>

<span data-ttu-id="51b32-107">*Record*. *Felder*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="51b32-107">*record*.*Fields*.CancelUpdate</span></span>

## <a name="remarks"></a><span data-ttu-id="51b32-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51b32-108">Remarks</span></span>

<span data-ttu-id="51b32-109">**Recordset**</span><span class="sxs-lookup"><span data-stu-id="51b32-109">**Recordset**</span></span>

<span data-ttu-id="51b32-p101">Verwenden Sie die **CancelUpdate** -Methode, um alle an der aktuellen Zeile vorgenommenen Änderungen abzubrechen oder eine neu hinzugefügte Zeile zu verwerfen. Sie können Änderungen an der aktuellen Zeile oder an einer neuen Zeile nach dem Aufrufen der **Update** -Methode nur abbrechen, wenn die Änderungen Teil einer Transaktion, für die Sie mit der [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Methode ein Rollback ausführen können, oder Teil einer Batchaktualisierung sind. Im Fall einer Batchaktualisierung können Sie die **Update** -Methode mit den Methoden **CancelUpdate** oder [CancelBatch](cancelbatch-method-ado.md) abbrechen.</span><span class="sxs-lookup"><span data-stu-id="51b32-p101">Use the **CancelUpdate** method to cancel any changes made to the current row or to discard a newly added row. You cannot cancel changes to the current row or a new row after you call the **Update** method, unless the changes are either part of a transaction that you can roll back with the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method, or part of a batch update. In the case of a batch update, you can cancel the **Update** with the **CancelUpdate** or [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="51b32-113">Wenn Sie eine neue Zeile hinzufügen, wenn Sie die **CancelUpdate** -Methode aufrufen, wird die Zeile, die vor dem [AddNew](addnew-method-ado.md)-Aufruf aktuell war, zur aktuellen Zeile.</span><span class="sxs-lookup"><span data-stu-id="51b32-113">If you are adding a new row when you call the **CancelUpdate** method, the current row becomes the row that was current before the [AddNew](addnew-method-ado.md) call.</span></span>

<span data-ttu-id="51b32-p102">Wenn Sie im Bearbeitungsmodus den aktuellen Datensatz verlassen möchten (z. B. mit [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) oder [Close](close-method-ado.md)), können Sie mit **CancelUpdate** alle ausstehenden Änderungen abbrechen. Möglicherweise müssen Sie dies tun, wenn die Aktualisierung nicht erfolgreich für die Datenquelle bereitgestellt werden kann (z. B. bleibt bei einem Löschversuch, der aufgrund von Verletzungen der referenziellen Integrität fehlschlägt, das **Recordset** nach einem Aufruf von [Delete](delete-method-ado-recordset.md) im Bearbeitungsmodus).</span><span class="sxs-lookup"><span data-stu-id="51b32-p102">If you are in edit mode and want to move off the current record (for example, with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md)), you can use **CancelUpdate** to cancel any pending changes. You may need to do this if the update cannot successfully be posted to the data source (for example, an attempted delete that fails due to referential integrity violations will leave the **Recordset** in edit mode after a call to [Delete](delete-method-ado-recordset.md)).</span></span>

<span data-ttu-id="51b32-116">**Record**</span><span class="sxs-lookup"><span data-stu-id="51b32-116">**Record**</span></span>

<span data-ttu-id="51b32-p103">Durch die **CancelUpdate** -Methode werden alle ausstehenden Einfügungen oder Löschungen von [Field](field-object-ado.md)-Objekten abgebrochen. Außerdem werden alle ausstehenden Aktualisierungen vorhandener Felder abgebrochen, und die Originalwerte der Felder werden wiederhergestellt. Die [Status](status-property-ado-recordset.md)-Eigenschaft aller Felder in der **Fields** -Auflistung wird auf **adFieldOK** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51b32-p103">The **CancelUpdate** method cancels any pending insertions or deletions of [Field](field-object-ado.md) objects, and cancels pending updates of existing fields and restores them to their original values. The [Status](status-property-ado-recordset.md) property of all fields in the **Fields** collection is set to **adFieldOK**.</span></span>

