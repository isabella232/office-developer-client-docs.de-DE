---
title: Field.ValidationRule-Eigenschaft (DAO)
TOCTitle: ValidationRule Property
ms:assetid: b07e644d-54d3-7199-6f99-178774e54398
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821784(v=office.15)
ms:contentKeyID: 48547123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0a5ec1c25e8364253143ea3379f4888ee65bddea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612169"
---
# <a name="fieldvalidationrule-property-dao"></a>Field.ValidationRule-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der die Daten in einem Feld direkt bei der Eingabe oder dem Hinzufügen zu einer Tabelle überprüft (gilt nur für Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . Validationrule

*Ausdruck* Ein Ausdruck, der ein **Field-Objekt** zurückgibt.

## <a name="remarks"></a>HinwBemerkungeneise

The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.

Die **ValidationRule**-Eigenschaft legt fest, ob ein Feld gültige Daten enthält. Wenn die Daten nicht gültig sind, tritt ein auffangbarer Laufzeitfehler auf. Die zurückgegebene Fehlermeldung ist der Text der **[ValidationText](field-validationtext-property-dao.md)** -Eigenschaft, sofern er angegeben wurde, oder der von **ValidationRule** angegebene Text.

Bei einem **[Field](field-object-dao.md)** -Objekt hängt die Verwendung der **ValidationRule**-Eigenschaft von dem Objekt ab, das die **Fields**-Auflistung enthält, an die das **Field**-Objekt angefügt wurde.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Zugehörigkeit zu Objekt</p></th>
<th><p>Nutzung</p></th>
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
<td><p><strong>Relation</strong></p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
</tbody>
</table>


Die Gültigkeitsprüfung wird nur für Datenbanken unterstützt, die die Microsoft Access-Datenbank-Engine verwenden.

Der von der **ValidationRule**-Eigenschaft eines **Field**-Objekts festgelegte Zeichenfolgenausdruck kann sich nur auf das betreffende **Field**-Objekt beziehen. Der Ausdruck kann sich nicht auf benutzerdefinierte Funktionen, SQL-Aggregatfunktionen oder Abfragen beziehen. Um die **ValidationRule**-Eigenschaft eines **Field**-Objekts festzulegen, wenn seine **ValidateOnSet**-Eigenschaft den Wert **True** hat, muss der Ausdruck erfolgreich analysiert werden (mit dem Feldnamen als impliziter Operand) und den Wert **True** ergeben. Wenn die **ValidateOnSet**-Eigenschaft des Objekts den Wert **False** hat, wird die **ValidationRule**-Einstellung ignoriert.


> [!NOTE]
> Wenn Sie die Eigenschaft auf eine Zeichenfolge festlegen, die mit einem Nicht-Ganzzahlwert verkettet ist, und die Systemparameter eine Nicht-USA angeben. Dezimalzeichen wie z. B. ein Komma (z. B. strRule = "PRICE &gt; " &amp; lngPrice und gifPrice = 125,50) führt zu einem Fehler, wenn Ihr Code versucht, Daten zu überprüfen. Dies liegt daran, dass der Wert während der Verkettung mithilfe des Standard-Dezimaltrennzeichens in eine Zeichenfolge konvertiert wird und SQL der Microsoft Access-Datenbank-Engine nur US-Dezimaltrennzeichen akzeptiert.


