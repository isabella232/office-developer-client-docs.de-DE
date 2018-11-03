---
title: Errors-Auflistung (ADO)
TOCTitle: Errors collection (ADO)
ms:assetid: 76c234b8-7fec-11c5-275e-864d5d880ee7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249486(v=office.15)
ms:contentKeyID: 48545706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a6462fed7054a66777a7957e2128b23a6fc0440f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929545"
---
# <a name="errors-collection-ado"></a><span data-ttu-id="b4920-102">Errors-Auflistung (ADO)</span><span class="sxs-lookup"><span data-stu-id="b4920-102">Errors collection (ADO)</span></span>


<span data-ttu-id="b4920-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4920-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4920-104">Enthält alle [Error](error-object-ado.md)-Objekte, die als Reaktion auf einen einzelnen anbieterbezogenen Fehler erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b4920-104">Contains all the [Error](error-object-ado.md) objects created in response to a single provider-related failure provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4920-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b4920-105">Remarks</span></span>

<span data-ttu-id="b4920-p101">Jeder Vorgang, an dem ADO-Objekte beteiligt sind, kann mindestens einen Anbieterfehler generieren. Sobald ein Fehler auftritt, kann mindestens ein **Error** -Objekt in der **Errors** -Auflistung des [Connection](connection-object-ado.md)-Objekts eingefügt werden. Wenn ein anderer ADO-Vorgang einen Fehler erzeugt, wird die **Errors** -Auflistung gelöscht, und die neue Gruppe der **Error** -Objekte kann in die **Errors** -Auflistung übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="b4920-p101">Any operation involving ADO objects can generate one or more provider errors. As each error occurs, one or more **Error** objects can be placed in the **Errors** collection of the [Connection](connection-object-ado.md) object. When another ADO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects can be placed in the **Errors** collection.</span></span>

<span data-ttu-id="b4920-p102">Jedes **Error** -Objekt stellt einen spezifischen Anbieterfehler dar und nicht einen ADO-Fehler. ADO-Fehler werden dem Ausnahmebehandlungsmechanismus der Laufzeitumgebung übergeben. In Microsoft Visual Basic verursacht das Auftreten eines ADO-spezifischen Fehlers z. B. ein [onError](onerror-event-rds.md)-Ereignis. Der Fehler wird im **Err** -Objekt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b4920-p102">Each **Error** object represents a specific provider error, not an ADO error. ADO errors are exposed to the run-time exception-handling mechanism. For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an [onError](onerror-event-rds.md) event and appear in the **Err** object.</span></span>

<span data-ttu-id="b4920-p103">ADO-Vorgänge, die keinen Fehler erzeugen, haben keine Auswirkung auf die **Errors** -Auflistung. Mit der [Clear](clear-method-ado.md)-Methode können Sie die **Errors** -Auflistung manuell löschen.</span><span class="sxs-lookup"><span data-stu-id="b4920-p103">ADO operations that don't generate an error have no effect on the **Errors** collection. Use the [Clear](clear-method-ado.md) method to manually clear the **Errors** collection.</span></span>

<span data-ttu-id="b4920-p104">Die Gruppe der **Error** -Objekte in der **Errors** -Auflistung beschreibt alle Fehler, die als Reaktion auf eine einzelne Anweisung aufgetreten sind. Wenn Sie die betreffenden Fehler in der **Errors** -Auflistung in einer Schleife durchlaufen, können die Fehlerbehandlungsroutinen die Ursache und den Ausgangspunkt eines Fehlers genauer feststellen und entsprechende Schritte zur Fehlerbehandlung vornehmen.</span><span class="sxs-lookup"><span data-stu-id="b4920-p104">The set of **Error** objects in the **Errors** collection describes all errors that occurred in response to a single statement. Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span></span>

<span data-ttu-id="b4920-p105">Von manchen Eigenschaften und Methoden werden Warnungen zurückgegeben, die als **Error** -Objekte in der **Errors** -Auflistung angezeigt werden, ohne dass die Ausführung eines Programms angehalten wird. Rufen Sie vor dem Aufrufen der Methoden [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) oder [CancelBatch](cancelbatch-method-ado.md) für ein [Recordset](recordset-object-ado.md)-Objekt oder der [Open](open-method-ado-connection.md)-Methode für ein **Connection** -Objekt oder vor dem Festlegen der [Filter](filter-property-ado.md)-Eigenschaft für ein **Recordset** -Objekt die **Clear** -Methode für die **Errors** -Auflistung auf. Auf diese Weise können Sie die [Count](count-property-ado.md)-Eigenschaft der **Errors** -Auflistung lesen, um auf zurückgegebene Warnungen zu testen.</span><span class="sxs-lookup"><span data-stu-id="b4920-p105">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution. Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, the [Open](open-method-ado-connection.md) method on a **Connection** object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection. That way you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>


> [!NOTE]
> <span data-ttu-id="b4920-119">[!HINWEIS] Weitere Informationen zur Art, wie ein einzelner ADO-Vorgang mehrere Fehler erzeugen kann, finden Sie in der Beschreibung des **Error** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="b4920-119">See the **Error** object topic for a more detailed explanation of the way a single ADO operation can generate multiple errors.</span></span>


