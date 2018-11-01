---
title: Status-Eigenschaft (ADO Field)
TOCTitle: Status Property (ADO Field)
ms:assetid: 7a7b45e8-2934-2e8e-77fa-a4f38272548d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249507(v=office.15)
ms:contentKeyID: 48545795
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6be229e2dfd0cc8dd25fd217bdd6cb50f65cb32
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872368"
---
# <a name="status-property-ado-field"></a>Status-Eigenschaft (ADO Field)


**Betrifft**: Access 2013, Office 2013

Gibt den Status eines [Field](field-object-ado.md)-Objekts an.

## <a name="return-value"></a>Rückgabewert

Gibt einen [FieldStatusEnum](fieldstatusenum.md)-Wert zurück. Der Standardwert lautet **AdFieldOK**.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt für Felder eines **Recordset**-Objekts stets [adFieldOK](recordset-object-ado.md) zurück.

Ergänzungen oder Löschungen in den [Fields](fields-collection-ado.md)-Auflistungen des [Record](record-object-ado.md)-Objekts werden bis zum Aufrufen der [Update](update-method-ado.md)-Methode zwischengespeichert. Mithilfe der **Status** -Eigenschaft können Sie die Felder ermitteln, die erfolgreich hinzugefügt oder gelöscht wurden.

Schemaänderungen werden zur Verbesserung der Leistung zwischengespeichert, bis **Update** aufgerufen wird, und klicken Sie dann die Änderungen in einer optimistischen Batchaktualisierung vorgenommen werden. Wenn die **Update** -Methode nicht aufgerufen wird, wird der Server nicht aktualisiert. Wenn keine Updates wird ein Fehler zurückgegeben, und die **Status** -Eigenschaft gibt die kombinierten Werte der Vorgang und Fehlerstatuscode an. Beispielsweise **AdFieldPendingInsert** **oder** **AdFieldPermissionDenied**. Die **Status** -Eigenschaft für jedes **Feld** kann verwendet werden, um zu ermitteln, warum das **Feld** nicht hinzugefügt, geändert oder gelöscht wurde. **Status** wird nur sinnvoll für den **Datensatz**angezeigt. **Fields** -Auflistung und nicht das **Recordset-Objekt**. **Fields** -Auflistung.

Zwei Probleme können auftreten, wenn hinzufügen, ändern oder Löschen eines **Felds**. Löscht der Benutzer auf ein **Feld**, wird es in der **Fields** -Auflistung zum Löschen gekennzeichnet. Das nachfolgende **Update** einen Fehler zurück, da der Benutzer versuchte, ein **Feld** zu löschen, für die sie nicht über die Berechtigung verfügen, wird das **Feld** Status **AdFieldPermissionDenied** **oder** **AdFieldPendingDelete**aufweisen. Aufrufen der [CancelUpdate](cancelupdate-method-ado.md) -Methode stellt ursprünglichen Werte wieder her und legt den **Status** auf **AdFieldOK**fest. Auf ähnliche Weise kann die **Update** -Methode einen Fehler zurück, da ein neues **Feld** hinzugefügt und einen Ungültiger Wert angegeben wurde. In diesem Fall wird das neue **Feld** in der **Fields** -Auflistung werden, und Sie haben den Status von **AdFieldPendingInsert** und vielleicht **AdFieldCantCreate**. Sie können einen entsprechenden Wert für das neue **Feld** angeben und erneut **Update** aufrufen. Beachten Sie, dass Aufruf von **Resync** stattdessen ist der Anbieter erforderlich.

