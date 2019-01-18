---
title: Recordset.MoveLast-Methode (DAO)
TOCTitle: MoveLast method
ms:assetid: fc0f7a33-1f55-9f5b-b00d-1b81f49b1c3e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837192(v=office.15)
ms:contentKeyID: 48548881
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 79799742499e163a43d51a2d8553adcadf27b36d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715270"
---
# <a name="recordsetmovelast-method-dao"></a>Recordset.MoveLast-Methode (DAO)

**Betrifft**: Access 2013, Office 2013

Wechselt zum letzten Datensatz in einem angegebenen **Recordset**-Objekt und macht diesen zum aktuellen Datensatz.

## <a name="syntax"></a>Syntax

*Ausdruck* . MoveLast (***Optionen***)

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich oder optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Options</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Auf <strong>dbRunAsync</strong> festgelegt, damit der Aufruf für <strong>MoveLast</strong> asynchron ausgeführt wird.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Move**-Methoden, um von einem Datensatz zum nächsten zu wechseln, ohne eine Bedingung anzuwenden.

Wenn Sie den aktuellen Datensatz bearbeiten, sollten Sie die Änderungen mit der **Update**-Methode speichern, bevor Sie zu einem anderen Datensatz wechseln. Ohne diese Aktualisierung gehen die Änderungen beim Wechseln zwischen Datensätzen ohne Warnung verloren.

Beim Öffnen eines **Recordset**-Objekts ist der erste Datensatz aktuell, und die **BOF**-Eigenschaft ist auf **False** festgelegt. Wenn **Recordset** keine Datensätze enthält, ist die **BOF**-Eigenschaft auf **True** festgelegt, und es ist kein aktueller Datensatz vorhanden.

Ist der erste bzw. letzte Datensatz beim Verwenden von **MoveFirst** oder **MoveLast** bereits aktuell, ändert sich der aktuelle Datensatz nicht.

Wenn Recordset vom Typ Tabelle **Recordset-Objekt** (nur Microsoft Access-Arbeitsbereiche) bezieht, folgt die Verschiebung den aktuellen Index. Sie können den aktuellen Index mit der **Index** -Eigenschaft festlegen. Wenn Sie den aktuellen Index nicht festlegen, ist die Reihenfolge der zurückgegebenen Datensätze nicht definiert.

> [!NOTE]
> Die **MoveLast** -Methode können Sie vollständig auffüllen einen Typ Dynaset oder Snapshot- **Recordset-Objekts** , um die aktuelle Anzahl der Datensätze im **Recordset-Objekt**enthalten. Jedoch, wenn Sie auf diese Weise **MoveLast** verwenden, können Sie die Leistung der Anwendung verlangsamen. Sie sollten nur **MoveLast** verwenden, um zählen der Datensätze abzurufen, wenn dies unbedingt erforderlich ist, erhalten Sie eine genaue Anzahl für ein neu geöffneten **Recordset-Objekt**ist. 
> 
> Wenn Sie die Konstante **DbRunAsync** mit **MoveLast**verwenden, ist der Methodenaufruf asynchron. Die **StillExecuting** -Eigenschaft können Sie bestimmen, wann **Recordset** vollständig aufgefüllt wird, und Sie können die **Cancel** -Methode verwenden, um die Ausführung des asynchronen Aufrufs **MoveLast** -Methode beendet werden.

Sie können nicht auf ein **Recordset** -Objekt weiterleiten – nur – Geben Sie die **MoveFirst**, **MoveLast**und **MovePrevious** -Methoden verwenden.

Verwenden Sie die **Move**-Methode, um die Position des aktuellen Datensatzes in einem **Recordset**-Objekt um eine bestimmte Anzahl von Datensätzen vorwärts oder rückwärts zu verschieben.

