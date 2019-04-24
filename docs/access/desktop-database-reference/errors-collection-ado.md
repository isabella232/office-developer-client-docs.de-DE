---
title: Errors-Auflistung (ADO)
TOCTitle: Errors collection (ADO)
ms:assetid: 76c234b8-7fec-11c5-275e-864d5d880ee7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249486(v=office.15)
ms:contentKeyID: 48545706
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: db9fa4fccc4f3d13849f34c157f2ea07cc3f171d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293427"
---
# <a name="errors-collection-ado"></a>Errors-Auflistung (ADO)


**Gilt für**: Access 2013, Office 2013

Enthält alle [Error](error-object-ado.md)-Objekte, die als Reaktion auf einen einzelnen anbieterbezogenen Fehler erstellt wurden.

## <a name="remarks"></a>Bemerkungen

Jeder Vorgang, an dem ADO-Objekte beteiligt sind, kann mindestens einen Anbieterfehler generieren. Sobald ein Fehler auftritt, kann mindestens ein **Error** -Objekt in der **Errors** -Auflistung des [Connection](connection-object-ado.md)-Objekts eingefügt werden. Wenn ein anderer ADO-Vorgang einen Fehler erzeugt, wird die **Errors** -Auflistung gelöscht, und die neue Gruppe der **Error** -Objekte kann in die **Errors** -Auflistung übernommen werden.

Jedes **Error** -Objekt stellt einen spezifischen Anbieterfehler dar und nicht einen ADO-Fehler. ADO-Fehler werden dem Ausnahmebehandlungsmechanismus der Laufzeitumgebung übergeben. In Microsoft Visual Basic verursacht das Auftreten eines ADO-spezifischen Fehlers z. B. ein [onError](onerror-event-rds.md)-Ereignis. Der Fehler wird im **Err** -Objekt angezeigt.

ADO-Vorgänge, die keinen Fehler erzeugen, haben keine Auswirkung auf die **Errors** -Auflistung. Mit der [Clear](clear-method-ado.md)-Methode können Sie die **Errors** -Auflistung manuell löschen.

Die Gruppe der **Error** -Objekte in der **Errors** -Auflistung beschreibt alle Fehler, die als Reaktion auf eine einzelne Anweisung aufgetreten sind. Wenn Sie die betreffenden Fehler in der **Errors** -Auflistung in einer Schleife durchlaufen, können die Fehlerbehandlungsroutinen die Ursache und den Ausgangspunkt eines Fehlers genauer feststellen und entsprechende Schritte zur Fehlerbehandlung vornehmen.

Von manchen Eigenschaften und Methoden werden Warnungen zurückgegeben, die als **Error** -Objekte in der **Errors** -Auflistung angezeigt werden, ohne dass die Ausführung eines Programms angehalten wird. Rufen Sie vor dem Aufrufen der Methoden [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) oder [CancelBatch](cancelbatch-method-ado.md) für ein [Recordset](recordset-object-ado.md)-Objekt oder der [Open](open-method-ado-connection.md)-Methode für ein **Connection** -Objekt oder vor dem Festlegen der [Filter](filter-property-ado.md)-Eigenschaft für ein **Recordset** -Objekt die **Clear** -Methode für die **Errors** -Auflistung auf. Auf diese Weise können Sie die [Count](count-property-ado.md)-Eigenschaft der **Errors** -Auflistung lesen, um auf zurückgegebene Warnungen zu testen.


> [!NOTE]
> [!HINWEIS] Weitere Informationen zur Art, wie ein einzelner ADO-Vorgang mehrere Fehler erzeugen kann, finden Sie in der Beschreibung des **Error** -Objekts.


