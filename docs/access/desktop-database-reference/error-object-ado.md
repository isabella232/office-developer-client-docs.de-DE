---
title: Error-Objekt – ActiveX Data Objects (ADO)
TOCTitle: Error object (ADO)
ms:assetid: 97e478bf-8b25-03a8-9358-abba5069cba3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249678(v=office.15)
ms:contentKeyID: 48546477
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a7c77a59368851f43b5e7bf2275f9f282546fb4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293483"
---
# <a name="error-object-ado"></a>Error-Objekt (ADO)


**Gilt für**: Access 2013, Office 2013

Enthält Details zu Datenzugriffsfehlern, die sich auf eine einzelne Operation beziehen, die den Anbieter betrifft.

## <a name="remarks"></a>Bemerkungen

Jeder Vorgang, an dem ADO-Objekte beteiligt sind, kann mindestens einen Anbieterfehler generieren. Sobald ein Fehler auftritt, wird mindestens ein **Error** -Objekt in der [Errors](errors-collection-ado.md)-Auflistung des [Connection](connection-object-ado.md)-Objekts eingefügt. Wenn ein anderer ADO-Vorgang einen Fehler erzeugt, wird die **Errors** -Auflistung gelöscht, und die neue Gruppe der **Error** -Objekte wird in die **Errors** -Auflistung übernommen.

> [!NOTE]
> [!HINWEIS] Jedes **Error** -Objekt stellt einen bestimmten Anbieterfehler dar und nicht einen ADO-Fehler. ADO-Fehler unterliegen dem Laufzeit-Fehlerbehandlungsmechanismus. In Microsoft Visual Basic löst das Auftreten eines ADO-spezifischen Fehlers z. B. ein **On Error** -Ereignis aus, und der Fehler wird im **Error** -Objekt angezeigt. Eine vollständige Liste der ADO-Fehler finden Sie unter dem Thema [ErrorValueEnum](errorvalueenum.md).

Sie können die Eigenschaften eines **Error** -Objekts lesen, um die folgenden Details über die einzelnen Fehler zu erhalten:

- Die [Description](description-property-ado.md)-Eigenschaft, die den Fehlertext enthält. Dies ist die Standardeigenschaft.

- Die [Number](number-property-ado.md)-Eigenschaft, die den **Long** -Ganzzahlwert der Fehlerkonstanten enthält.

- Die [Source](source-property-ado-error.md)-Eigenschaft, die das Objekt identifiziert, das den Fehler ausgelöst hat. Diese Eigenschaft ist besonders nützlich, wenn nach einer Abfrage einer Datenquelle mehrere **Error** -Objekte in der **Errors** -Auflistung enthalten sind.

- Die Eigenschaften [SQLState](sqlstate-property-ado.md) und [NativeError](nativeerror-property-ado.md), die Informationen über SQL-Datenquellen bereitstellen.

Wenn ein Anbieterfehler auftritt, wird er in die **Errors** -Auflistung des **Connection** -Objekts aufgenommen. ADO unterstützt die Rückgabe mehrerer Fehler durch einen einzelnen ADO-Vorgang, um anbieterspezifische Fehlerinformationen zu gestatten. Verwenden Sie die zutreffenden Fehlerbehandlungsfeatures der Sprache oder Umgebung, und durchlaufen Sie dann die Eigenschaften der einzelnen **Error** -Objekte in der **Errors** -Auflistung in geschachtelten Schleifen, um diese ausführlichen Fehlerinformationen in einer Fehlerbehandlungsroutine zu erhalten.

**Microsoft Visual Basic-und VBScript-Benutzer** Wenn kein gültiges **Connection** -Objekt vorhanden ist, müssen Sie Fehlerinformationen aus dem **Error** -Objekt abrufen.

Wie andere Anbieter löscht auch ADO das **OLE Error Info** -Objekt vor dem Ausführen eines Aufrufs, der potenziell einen neuen Anbieterfehler erzeugen könnte. Die **Errors** -Auflistung des **Connection** -Objekts wird jedoch gelöscht und nur dann aufgefüllt, wenn der Anbieter einen neuen Fehler erzeugt, oder wenn die [Clear](clear-method-ado.md)-Methode aufgerufen wird.

Von manchen Eigenschaften und Methoden werden Warnungen zurückgegeben, die als **Error** -Objekte in der **Errors** -Auflistung angezeigt werden, ohne dass die Ausführung eines Programms angehalten wird. Rufen Sie vor dem Aufrufen der Methoden [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) oder [CancelBatch](cancelbatch-method-ado.md) für ein [Recordset](recordset-object-ado.md)-Objekt oder der [Open](open-method-ado-connection.md)-Methode für ein **Connection** -Objekt oder vor dem Festlegen der [Filter](filter-property-ado.md)-Eigenschaft für ein **Recordset** -Objekt die **Clear** -Methode für die **Errors** -Auflistung auf. Auf diese Weise können Sie die [Count](count-property-ado.md)-Eigenschaft der **Errors** -Auflistung lesen, um auf zurückgegebene Warnungen zu testen.

