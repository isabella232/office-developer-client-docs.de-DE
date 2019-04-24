---
title: Field2. ValidationRule-Eigenschaft (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e9e50148f4b87a957ff2317b1b39522d7d4e1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292650"
---
# <a name="field2validationrule-property-dao"></a>Field2. ValidationRule-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der die Daten in einem Feld direkt bei der Eingabe oder dem Hinzufügen zu einer Tabelle überprüft (gilt nur für Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . ValidationRule

*Ausdruck* Ein Ausdruck, der ein **Field2** -Objekt zurückgibt.

## <a name="remarks"></a>Bemerkungen

The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.

Die **ValidationRule**-Eigenschaft bestimmt, ob ein Feld gültige Daten enthält. Sind die Daten nicht gültig, tritt ein abfangbarer Fehler auf. Die zurückgegebene Fehlermeldung ist der Text der **ValidationText**-Eigenschaft, falls angegeben, oder der Text des von der **ValidationRule**-Eigenschaft angegebenen Ausdrucks.

Bei einem **Field2**-Objekt hängt die Verwendung der **ValidationRule**-Eigenschaft vom Objekt ab, das die **Fields**-Auflistung enthält, der das **Field2**-Objekt angefügt wird.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Zugehörigkeit zu Objekt</p></th>
<th><p>Verwendung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong></p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="even">
<td><p><strong>Beziehung</strong></p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
</tbody>
</table>


Die Überprüfung wird nur für Datenbanken unterstützt, die das Microsoft Access-Datenbankmodul verwenden.

Der von der **ValidationRule**-Eigenschaft eines **Field2**-Objekts angegebene Zeichenfolgenausdruck kann sich nur auf dieses **Field2**-Objekt beziehen. Der Ausdruck kann sich nicht auf benutzerdefinierte Funktionen, SQL-Aggregatfunktionen oder Abfragen beziehen. Damit die **ValidationRule**-Eigenschaft eines **Field2**-Objekts festgelegt werden kann, wenn die Einstellung seiner **ValidateOnSet**-Eigenschaft auf **True** festgelegt ist, muss der Ausdruck erfolgreich analysiert (wobei der Feldname ein impliziter Operand sein muss) und mit **True** ausgewertet worden sein. Ist die Einstellung seiner **ValidateOnSet**-Eigenschaft auf **False** festgelegt, wird die Einstellung der **ValidationRule**-Eigenschaft ignoriert.


> [!NOTE]
> Wenn Sie die-Eigenschaft auf eine Zeichenfolge festlegen, die mit einem nicht-ganzzahligen Wert verkettet ist, und die Systemparameter ein nicht-U. S. Decimal-Zeichen wie ein Komma (beispielsweise strRule &gt; = &amp; "Price" lngPrice und lngPrice = 125, 50) angeben, tritt ein Fehler auf, wenn Ihr Code versucht, alle Daten zu überprüfen. Dies liegt daran, dass der Wert während der Verkettung mithilfe des Standard-Dezimaltrennzeichens in eine Zeichenfolge konvertiert wird und SQL der Microsoft Access-Datenbank-Engine nur US-Dezimaltrennzeichen akzeptiert.


