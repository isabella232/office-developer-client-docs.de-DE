---
title: Recordset2. BOF-Eigenschaft (DAO)
TOCTitle: BOF Property
ms:assetid: d97d0507-0d5a-e3f1-fa30-40caec9f3ffa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835098(v=office.15)
ms:contentKeyID: 48548053
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5ffe9c679da3f11666799caa070f51f384729cc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307462"
---
# <a name="recordset2bof-property-dao"></a>Recordset2. BOF-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt einen Wert zurück, der angibt, ob die aktuelle Datensatzposition in einem **Recordset**-Objekt vor dem ersten Datensatz liegt. Schreibgeschützter **Boolean**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . BOF

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Mit den Eigenschaften **BOF** und **EOF** können Sie feststellen, ob ein **Recordset**-Objekt Datensätze enthält oder ob Sie beim Wechsel zwischen Datensätzen über die Grenzen eines **Recordset**-Objekts navigiert sind.

Die Position des aktuellen Datensatzzeigers legt die Rückgabewerte von **BOF** und **EOF** fest.

Wenn die **BOF**- oder die **EOF**-Eigenschaft **True** ist, gibt es keinen aktuellen Datensatz.

If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True**, and the **Recordset** object's **RecordCount** property setting is 0. When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**; they remain **False** until you move beyond the beginning or end of the **Recordset** object by using the **MovePrevious** or **MoveNext** method, respectively. When you move beyond the beginning or end of the recordset, there is no current record or no record exists.

Wenn Sie den letzten verbleibenden Datensatz im **Recordset**-Objekt löschen, bleiben die Eigenschaften **BOF**BOF und **EOF**EOF so lange **False**False, bis Sie versuchen, den aktuellen Datensatz neu zu positionieren.

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

Wenn Sie in einem Microsoft Access-Arbeitsbereich einem leeren Recordset einen Datensatz hinzufügen, wird die **BOF**-Eigenschaft auf **False** festgelegt, **EOF** bleibt jedoch **True** und gibt dadurch an, dass sich die aktuelle Position am Ende des Recordsets befindet.

Any **Delete** method, even if it removes the only remaining record from a recordset, won't change the setting of the **BOF** or **EOF** property.

The following table shows how Move methods that don't locate a record affect the **BOF** and **EOF** property settings.

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

