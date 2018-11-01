---
title: Error-Objekt - ActiveX Data Objects (ADO)
TOCTitle: Error Object (ADO)
ms:assetid: 97e478bf-8b25-03a8-9358-abba5069cba3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249678(v=office.15)
ms:contentKeyID: 48546477
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ae89c4d2300b167a8e7b993ad8830838d91f0617
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877023"
---
# <a name="error-object-ado"></a><span data-ttu-id="fba09-102">Error-Objekt (ADO)</span><span class="sxs-lookup"><span data-stu-id="fba09-102">Error Object (ADO)</span></span>


<span data-ttu-id="fba09-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fba09-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fba09-104">Enthält Details zu Datenzugriffsfehlern, die sich auf eine einzelne Operation beziehen, die den Anbieter betrifft.</span><span class="sxs-lookup"><span data-stu-id="fba09-104">Contains details about data access errors that pertain to a single operation involving the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="fba09-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fba09-105">Remarks</span></span>

<span data-ttu-id="fba09-p101">Jeder Vorgang, an dem ADO-Objekte beteiligt sind, kann mindestens einen Anbieterfehler generieren. Sobald ein Fehler auftritt, wird mindestens ein **Error** -Objekt in der [Errors](errors-collection-ado.md)-Auflistung des [Connection](connection-object-ado.md)-Objekts eingefügt. Wenn ein anderer ADO-Vorgang einen Fehler erzeugt, wird die **Errors** -Auflistung gelöscht, und die neue Gruppe der **Error** -Objekte wird in die **Errors** -Auflistung übernommen.</span><span class="sxs-lookup"><span data-stu-id="fba09-p101">Any operation involving ADO objects can generate one or more provider errors. As each error occurs, one or more **Error** objects are placed in the [Errors](errors-collection-ado.md) collection of the [Connection](connection-object-ado.md) object. When another ADO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects is placed in the **Errors** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="fba09-p102">[!HINWEIS] Jedes **Error** -Objekt stellt einen bestimmten Anbieterfehler dar und nicht einen ADO-Fehler. ADO-Fehler unterliegen dem Laufzeit-Fehlerbehandlungsmechanismus. In Microsoft Visual Basic löst das Auftreten eines ADO-spezifischen Fehlers z. B. ein **On Error** -Ereignis aus, und der Fehler wird im **Error** -Objekt angezeigt. Eine vollständige Liste der ADO-Fehler finden Sie unter dem Thema [ErrorValueEnum](errorvalueenum.md).</span><span class="sxs-lookup"><span data-stu-id="fba09-p102">Each **Error** object represents a specific provider error, not an ADO error. ADO errors are exposed to the run-time exception-handling mechanism. For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an **On Error** event and appear in the **Error** object. For a complete list of ADO errors, see the [ErrorValueEnum](errorvalueenum.md) topic.</span></span>

<span data-ttu-id="fba09-113">Sie können die Eigenschaften eines **Error** -Objekts lesen, um die folgenden Details über die einzelnen Fehler zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="fba09-113">You can read an **Error** object's properties to obtain specific details about each error, including the following:</span></span>

- <span data-ttu-id="fba09-p103">Die [Description](description-property-ado.md)-Eigenschaft, die den Fehlertext enthält. Dies ist die Standardeigenschaft.</span><span class="sxs-lookup"><span data-stu-id="fba09-p103">The [Description](description-property-ado.md) property, which contains the text of the error. This is the default property.</span></span>

- <span data-ttu-id="fba09-116">Die [Number](number-property-ado.md)-Eigenschaft, die den **Long** -Ganzzahlwert der Fehlerkonstanten enthält.</span><span class="sxs-lookup"><span data-stu-id="fba09-116">The [Number](number-property-ado.md) property, which contains the **Long** integer value of the error constant.</span></span>

- <span data-ttu-id="fba09-p104">Die [Source](source-property-ado-error.md)-Eigenschaft, die das Objekt identifiziert, das den Fehler ausgelöst hat. Diese Eigenschaft ist besonders nützlich, wenn nach einer Abfrage einer Datenquelle mehrere **Error** -Objekte in der **Errors** -Auflistung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="fba09-p104">The [Source](source-property-ado-error.md) property, which identifies the object that raised the error. This is particularly useful when you have several **Error** objects in the **Errors** collection following a request to a data source.</span></span>

- <span data-ttu-id="fba09-119">Die Eigenschaften [SQLState](sqlstate-property-ado.md) und [NativeError](nativeerror-property-ado.md), die Informationen über SQL-Datenquellen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fba09-119">The [SQLState](sqlstate-property-ado.md) and [NativeError](nativeerror-property-ado.md) properties, which provide information from SQL data sources.</span></span>

<span data-ttu-id="fba09-p105">Wenn ein Anbieterfehler auftritt, wird er in die **Errors** -Auflistung des **Connection** -Objekts aufgenommen. ADO unterstützt die Rückgabe mehrerer Fehler durch einen einzelnen ADO-Vorgang, um anbieterspezifische Fehlerinformationen zu gestatten. Verwenden Sie die zutreffenden Fehlerbehandlungsfeatures der Sprache oder Umgebung, und durchlaufen Sie dann die Eigenschaften der einzelnen **Error** -Objekte in der **Errors** -Auflistung in geschachtelten Schleifen, um diese ausführlichen Fehlerinformationen in einer Fehlerbehandlungsroutine zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fba09-p105">When a provider error occurs, it is placed in the **Errors** collection of the **Connection** object. ADO supports the return of multiple errors by a single ADO operation to allow for error information specific to the provider. To obtain this rich error information in an error handler, use the appropriate error-trapping features of the language or environment you are working with, then use nested loops to enumerate the properties of each **Error** object in the **Errors** collection.</span></span>

<span data-ttu-id="fba09-123">**Microsoft Visual Basic- und VBScript-Benutzer** Wenn kein gültiges **Connection** -Objekt vorhanden ist, müssen Sie Fehlerinformationen aus dem **Error** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fba09-123">**Microsoft Visual Basic and VBScript Users**If there is no valid **Connection** object, you will need to retrieve error information from the **Error** object.</span></span>

<span data-ttu-id="fba09-p106">Wie andere Anbieter löscht auch ADO das **OLE Error Info** -Objekt vor dem Ausführen eines Aufrufs, der potenziell einen neuen Anbieterfehler erzeugen könnte. Die **Errors** -Auflistung des **Connection** -Objekts wird jedoch gelöscht und nur dann aufgefüllt, wenn der Anbieter einen neuen Fehler erzeugt, oder wenn die [Clear](clear-method-ado.md)-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fba09-p106">Just as providers do, ADO clears the **OLE Error Info** object before making a call that could potentially generate a new provider error. However, the **Errors** collection on the **Connection** object is cleared and populated only when the provider generates a new error, or when the [Clear](clear-method-ado.md) method is called.</span></span>

<span data-ttu-id="fba09-p107">Von manchen Eigenschaften und Methoden werden Warnungen zurückgegeben, die als **Error** -Objekte in der **Errors** -Auflistung angezeigt werden, ohne dass die Ausführung eines Programms angehalten wird. Rufen Sie vor dem Aufrufen der Methoden [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) oder [CancelBatch](cancelbatch-method-ado.md) für ein [Recordset](recordset-object-ado.md)-Objekt oder der [Open](open-method-ado-connection.md)-Methode für ein **Connection** -Objekt oder vor dem Festlegen der [Filter](filter-property-ado.md)-Eigenschaft für ein **Recordset** -Objekt die **Clear** -Methode für die **Errors** -Auflistung auf. Auf diese Weise können Sie die [Count](count-property-ado.md)-Eigenschaft der **Errors** -Auflistung lesen, um auf zurückgegebene Warnungen zu testen.</span><span class="sxs-lookup"><span data-stu-id="fba09-p107">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution. Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object; the [Open](open-method-ado-connection.md) method on a **Connection** object; or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection. That way, you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>

