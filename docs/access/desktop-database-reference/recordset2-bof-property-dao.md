---
title: Recordset2.BOF Property (DAO)
TOCTitle: BOF Property
ms:assetid: d97d0507-0d5a-e3f1-fa30-40caec9f3ffa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835098(v=office.15)
ms:contentKeyID: 48548053
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9e85b86d2ccfeaddd56f5373684e8790ee1ab0b2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876421"
---
# <a name="recordset2bof-property-dao"></a>Recordset2.BOF Property (DAO)


**Betrifft**: Access 2013, Office 2013

Gibt einen Wert zurück, der angibt, ob die aktuelle Datensatzposition in einem **Recordset** -Objekt vor dem ersten Datensatz liegt. Schreibgeschützter **Boolean** -Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . BOF-EIGENSCHAFT

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Mit den Eigenschaften **BOF** und **EOF** können Sie feststellen, ob ein **Recordset**-Objekt Datensätze enthält oder ob Sie beim Wechsel zwischen Datensätzen über die Grenzen eines **Recordset**-Objekts navigiert sind.

Die Position des aktuellen Datensatzzeigers legt die Rückgabewerte von **BOF** und **EOF** fest.

Wenn die **BOF**- oder die **EOF**-Eigenschaft **True** ist, gibt es keinen aktuellen Datensatz.

Wenn Sie ein **Recordset** -Objekt öffnen, die keine Datensätze enthält die Eigenschaften **BOF** und **EOF** auf **True**festgelegt sind, und Einstellung für das **Recordset** -Objekt **RecordCount** -Eigenschaft ist 0. Beim Öffnen eines **Recordset** -Objekts, das mindestens einen Datensatz enthält, wird der erste Datensatz der aktuelle Datensatz ist und die Eigenschaften **BOF** und **EOF** sind **False**; Sie verbleiben **False** , bis Sie außerhalb der Anfang oder das Ende des **Recordset** -Objekts verschieben, indem Sie mithilfe von der **MovePrevious** oder die **MoveNext** -Methode. Wenn Sie über den Anfang oder das Ende des Recordset-Objekts verschieben, kein aktueller Datensatz vorhanden ist oder kein Datensatz vorhanden ist.

Wenn Sie den letzten verbleibenden Datensatz im **Recordset**-Objekt löschen, bleiben die Eigenschaften **BOF**BOF und **EOF**EOF so lange **False**False, bis Sie versuchen, den aktuellen Datensatz neu zu positionieren.

Wenn Sie die **MoveLast**-Methode auf ein **Recordset**-Objekt anwenden, das Datensätze enthält, wird der letzte Datensatz zum aktuellen Datensatz. Wenn Sie dann die **MoveNext**-Methode verwenden, wird der aktuelle Datensatz ungültig und die **EOF**-Eigenschaft wird auf **True** festgelegt. Wenn Sie dagegen die **MoveFirst**-Methode auf ein **Recordset**-Objekt anwenden, das Datensätze enthält, wird der erste Datensatz zum aktuellen Datensatz. Wenn Sie dann die **MovePrevious**-Methode verwenden, gibt es keinen aktuellen Datensatz, und die **BOF**-Eigenschaft erhält den Wert **True**.

Wenn Sie alle Datensätze in einem **Recordset**-Objekt verwenden, durchsucht Ihr Code gewöhnlich unter Verwendung der **MoveNext**-Methode die Datensätze, bis die **EOF**-Eigenschaft den Wert **True** hat.

Wenn Sie die **MoveNext**-Methode verwenden, während die **EOF**-Eigenschaft den Wert **True** hat, oder wenn Sie die **MovePrevious**-Methode verwenden, während die **BOF**-Eigenschaft den Wert **True** hat, tritt ein Fehler auf.

In dieser Tabelle ist dargestellt, welche Move-Methoden für verschiedene Kombinationen der Eigenschaften **BOF** und **EOF** zulässig sind.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>MoveFirst,<br />
MoveLast</p></th>
<th><p>MovePrevious,<br />
Verschieben von &lt; 0</p></th>
<th><p><br />
Move 0</p></th>
<th><p>MoveNext,<br />
Verschieben von &gt; 0</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>BOF = "true"</strong><br />
<strong>EOF = False</strong></p></td>
<td><p>Zulässig</p></td>
<td><p>Fehler</p></td>
<td><p>Fehler</p></td>
<td><p>Zulässig</p></td>
</tr>
<tr class="even">
<td><p><strong>BOF = "false"</strong><br />
<strong>EOF = True</strong></p></td>
<td><p>Zulässig</p></td>
<td><p>Zulässig</p></td>
<td><p>Fehler</p></td>
<td><p>Fehler</p></td>
</tr>
<tr class="odd">
<td><p>Beide <strong>True</strong></p></td>
<td><p>Fehler</p></td>
<td><p>Fehler</p></td>
<td><p>Fehler</p></td>
<td><p>Fehler</p></td>
</tr>
<tr class="even">
<td><p>Beide <strong>False</strong></p></td>
<td><p>Zulässig</p></td>
<td><p>Zulässig</p></td>
<td><p>Zulässig</p></td>
<td><p>Zulässig</p></td>
</tr>
</tbody>
</table>


Wenn eine Move-Methode zulässig ist, heißt das nicht, dass die Methode einen Datensatz findet. Es bedeutet nur, dass die Ausführung der betreffenden Move-Methode gestattet ist und keinen Fehler generiert. Der Status der Eigenschaften **BOF** und **EOF** kann sich durch die versuchte Ausführung der Move-Methode ändern.

Eine **OpenRecordset**-Methode ruft intern eine **MoveFirst**-Methode auf. Wenn Sie daher eine **OpenRecordset**-Methode auf eine leere Gruppe von Datensätzen anwenden, werden die Eigenschaften **BOF** und **EOF** auf **True** gesetzt. (In der folgenden Tabelle ist das Verhalten einer fehlgeschlagenen **MoveFirst**-Methode aufgeführt.)

Alle Move-Methoden, die einen Datensatz erfolgreich finden, legen für die Eigenschaften **BOF** und **EOF** den Wert **False** fest.

Wenn Sie in einem Microsoft Access-Arbeitsbereich einem leeren Recordset einen Datensatz hinzufügen, wird die **BOF**-Eigenschaft auf **False** festgelegt, **EOF** bleibt jedoch **True** und gibt dadurch an, dass sich die aktuelle Position am Ende des Recordsets befindet.

Jede Methode **Löschen** wird nicht, auch wenn er den letzte Datensatz aus einem Recordset-Objekt entfernt die Einstellung der **Eigenschaften BOF** oder **EOF** -Eigenschaft ändern.

Die folgende Tabelle zeigt, welche Auswirkungen Move-Methoden, bei denen ein Datensatz nicht gefunden wird, auf die Einstellungen der Eigenschaften **BOF** und **EOF** haben.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>BOF</p></th>
<th><p>EOF</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>MoveFirst</strong>, <strong>MoveLast</strong></p></td>
<td><p><strong>True</strong></p></td>
<td><p><strong>True</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Move</strong> 0</p></td>
<td><p>Keine Änderung</p></td>
<td><p>Keine Änderung</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>, <strong>Verschieben Sie</strong> &lt; 0</p></td>
<td><p><strong>True</strong></p></td>
<td><p>Keine Änderung</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>, <strong>Verschieben Sie</strong> &gt; 0</p></td>
<td><p>Keine Änderung</p></td>
<td><p><strong>True</strong></p></td>
</tr>
</tbody>
</table>

