---
title: Recordset2. EOF-Eigenschaft (DAO)
TOCTitle: EOF Property
ms:assetid: 9d4e1ee2-e866-3ebf-e08b-b31b0cb47ed9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198245(v=office.15)
ms:contentKeyID: 48546622
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052886
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2d328160b6c88de61a041c54bcd6f305b73c26da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309443"
---
# <a name="recordset2eof-property-dao"></a>Recordset2. EOF-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt einen Wert zurück, der angibt, ob die aktuelle Datensatzposition hinter dem letzten Datensatz in einem **Recordset**-Objekt liegt. Schreibgeschützter **Boolean**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . EOF

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Mit den Eigenschaften **BOF** und **EOF** können Sie feststellen, ob ein **Recordset**-Objekt Datensätze enthält oder ob Sie beim Wechsel zwischen Datensätzen über die Grenzen eines **Recordset**-Objekts navigiert sind.

Die Position des aktuellen Datensatzzeigers legt die Rückgabewerte von **BOF** und **EOF** fest.

Wenn die **BOF**- oder die **EOF**-Eigenschaft **True** ist, gibt es keinen aktuellen Datensatz.

Wenn Sie ein **Recordset**-Objekt öffnen, das keine Datensätze enthält, erhalten die Eigenschaften **BOF** und **EOF** den Wert **True**, und der Wert der **RecordCount**-Eigenschaft des **Recordset**-Objekts wird auf 0 festgelegt. Wenn Sie ein **Recordset**-Objekt öffnen, das mindestens einen Datensatz enthält, ist der erste Datensatz der aktuelle Datensatz und die Eigenschaften **BOF** und **EOF** haben den Wert **False**. Die Einstellung **False** wird beibehalten, bis Sie vor den Anfang oder hinter das Ende des **Recordset**-Objekts navigieren oder die **MovePrevious**- oder **MoveNext**-Methode verwenden. Wenn Sie vor den Anfang oder hinter das Ende des **Recordset**-Objekts navigieren, gibt es keinen aktuellen Datensatz.

Wenn Sie den letzten verbleibenden Datensatz im **Recordset**-Objekt löschen, bleiben die Eigenschaften **BOF** und **EOF** so lange **False**, bis Sie versuchen, den aktuellen Datensatz neu zu positionieren.

Wenn Sie die **MoveLast**-Methode auf ein **Recordset**-Objekt anwenden, das Datensätze enthält, wird der letzte Datensatz zum aktuellen Datensatz. Wenn Sie dann die **MoveNext**-Methode verwenden, wird der aktuelle Datensatz ungültig, und die **EOF**-Eigenschaft wird auf **True** festgelegt. Wenn Sie dagegen die **MoveFirst**-Methode auf ein **Recordset**-Objekt anwenden, das Datensätze enthält, wird der erste Datensatz zum aktuellen Datensatz. Wenn Sie dann die **MovePrevious**-Methode verwenden, gibt es keinen aktuellen Datensatz, und die **BOF**-Eigenschaft erhält den Wert **True**.

Wenn Sie alle Datensätze in einem **Recordset**-Objekt verwenden, durchsucht Ihr Code gewöhnlich unter Verwendung der **MoveNext**-Methode die Datensätze, bis die **EOF**-Eigenschaft den Wert **True** hat.

Wenn Sie die **MoveNext**-Methode verwenden, während die **EOF**-Eigenschaft den Wert **True** hat, oder wenn Sie die **MovePrevious**-Methode verwenden, während die **BOF**-Eigenschaft den Wert **True** hat, tritt ein Fehler auf.

This table shows which Move methods are allowed with different combinations of the **BOF** and **EOF** properties.

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
<th><p>MoveFirst<br />
MoveLast</p></th>
<th><p>MovePrevious<br />
Verschieben &lt; 0</p></th>
<th><p><br />
Move 0</p></th>
<th><p>MoveNext<br />
Verschieben &gt; 0</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>BOF = true,</strong><br />
<strong>EOF = false</strong></p></td>
<td><p>Allowed</p></td>
<td><p>Fehler</p></td>
<td><p>Fehler</p></td>
<td><p>Allowed</p></td>
</tr>
<tr class="even">
<td><p><strong>BOF = false,</strong><br />
<strong>EOF = true</strong></p></td>
<td><p>Allowed</p></td>
<td><p>Allowed</p></td>
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
<td><p>Allowed</p></td>
<td><p>Allowed</p></td>
<td><p>Zulässig</p></td>
</tr>
</tbody>
</table>


Wenn eine Move-Methode zulässig ist, heißt das nicht, dass die Methode einen Datensatz findet. Es bedeutet nur, dass die Ausführung der betreffenden Move-Methode gestattet ist und keinen Fehler generiert. Der Status der Eigenschaften **BOF** und **EOF** kann sich durch die versuchte Ausführung der Move-Methode ändern.

Eine **OpenRecordset**-Methode ruft intern eine **MoveFirst**-Methode auf. Wenn Sie daher eine **OpenRecordset**-Methode auf eine leere Gruppe von Datensätzen anwenden, werden die Eigenschaften **BOF** und **EOF** auf **True** gesetzt. (In der folgenden Tabelle ist das Verhalten einer fehlgeschlagenen **MoveFirst**-Methode aufgeführt.)

All Move methods that successfully locate a record will set both **BOF** and **EOF** to **False**.

Wenn Sie in einem Microsoft Access-Arbeitsbereich einem leeren **Recordset**-Objekt einen Datensatz hinzufügen, wird die **BOF**-Eigenschaft auf **False** festgelegt, **EOF** bleibt jedoch **True** und gibt dadurch an, dass sich die aktuelle Position am Ende des **Recordset**-Objekts befindet.

**Delete**-Methoden ändern in keinem Fall die Einstellung der Eigenschaften **BOF** und **EOF**, selbst wenn durch die Methode der letzte Datensatz aus einem **Recordset**-Objekt entfernt wird.

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
<td><p><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</p></td>
<td><p><strong>True</strong></p></td>
<td><p>Keine Änderung</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</p></td>
<td><p>Keine Änderung</p></td>
<td><p><strong>True</strong></p></td>
</tr>
</tbody>
</table>

