---
title: Recordset.MoveLast Method (DAO)
TOCTitle: MoveLast Method
ms:assetid: fc0f7a33-1f55-9f5b-b00d-1b81f49b1c3e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837192(v=office.15)
ms:contentKeyID: 48548881
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c154a576a4ac1aedf555ba8164bc243fe49a3841
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474848"
---
# <a name="recordsetmovelast-method-dao"></a>Recordset.MoveLast Method (DAO)


**Betrifft**: Access 2013 | Office 2013

Wechselt zum letzten Datensatz in einem angegebenen **Recordset**-Objekt und macht diesen zum aktuellen Datensatz.

## <a name="syntax"></a>Syntax

*Ausdruck* . MoveLast (***Optionen***)

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

### <a name="parameters"></a>Parameter

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
<th><p>Erforderlich/Optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Optionen</p></td>
<td><p>Optional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Auf <strong>dbRunAsync</strong> festgelegt, damit der Aufruf für <strong>MoveLast</strong> asynchron ausgeführt wird.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Verwenden Sie die **Move**-Methoden, um von einem Datensatz zum nächsten zu wechseln, ohne eine Bedingung anzuwenden.

Wenn Sie den aktuellen Datensatz bearbeiten, sollten Sie die Änderungen mit der **Update**-Methode speichern, bevor Sie zu einem anderen Datensatz wechseln. Ohne diese Aktualisierung gehen die Änderungen beim Wechseln zwischen Datensätzen ohne Warnung verloren.

Beim Öffnen eines **Recordset**-Objekts ist der erste Datensatz aktuell, und die **BOF**-Eigenschaft ist auf **False** festgelegt. Wenn **Recordset** keine Datensätze enthält, ist die **BOF**-Eigenschaft auf **True** festgelegt, und es ist kein aktueller Datensatz vorhanden.

Ist der erste bzw. letzte Datensatz beim Verwenden von **MoveFirst** oder **MoveLast** bereits aktuell, ändert sich der aktuelle Datensatz nicht.

Wenn Recordset vom Typ Tabelle **Recordset-Objekt** (nur Microsoft Access-Arbeitsbereiche) bezieht, folgt die Verschiebung den aktuellen Index. Sie können den aktuellen Index mit der **Index** -Eigenschaft festlegen. Wenn Sie den aktuellen Index nicht festlegen, ist die Reihenfolge der zurückgegebenen Datensätze nicht definiert.


> [!NOTE]
> <P>Mithilfe der MoveLast-Methode können Sie ein Recordset vom Typ Dynaset oder Snapshot vollständig auffüllen, um die aktuelle Anzahl von Datensätzen im Recordset anzugeben. Wenn Sie allerdings MoveLast auf diese Weise verwenden, kann dies die Leistung der Anwendung beeinträchtigen. Sie sollten nur dann mithilfe von MoveLast eine Datensatzanzahl abrufen, wenn Sie unbedingt eine genaue Anzahl für ein neu geöffnetes Recordset benötigen. Wenn Sie die dbRunAsync-Konstante mit MoveLast verwenden, ist der Methodenaufruf asynchron. Sie können die StillExecuting-Eigenschaft verwenden, um festzustellen, ob das Recordset vollständig aufgefüllt ist. Mit der Cancel-Methode beenden Sie die Ausführung des asynchronen MoveLast-Methodenaufrufs.</P>



Sie können nicht auf ein **Recordset** -Objekt weiterleiten – nur – Geben Sie die **MoveFirst**, **MoveLast**und **MovePrevious** -Methoden verwenden.

Verwenden Sie die **Move**-Methode, um die Position des aktuellen Datensatzes in einem **Recordset**-Objekt um eine bestimmte Anzahl von Datensätzen vorwärts oder rückwärts zu verschieben.

