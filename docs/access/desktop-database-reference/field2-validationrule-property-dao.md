---
title: Field2.ValidationRule Property (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc2e2bee3a459c2f2b25b26bba4ca2fadd7fb945
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473766"
---
# <a name="field2validationrule-property-dao"></a>Field2.ValidationRule Property (DAO)


**Betrifft**: Access 2013 | Office 2013

Legt einen Wert fest, der die Daten in einem Feld überprüft, wenn es geändert oder einer Tabelle hinzugefügt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . ValidationRule

*Ausdruck* Ein Ausdruck, der ein **Field2** -Objekt zurückgibt.

## <a name="remarks"></a>Bemerkungen

Die Einstellungen oder Rückgabewerte ist eine Zeichenfolge, die einen Vergleich in der Form einer SQL WHERE-Klausel ohne das WHERE reservierte Wort beschreibt. Für ein Objekt, das noch nicht an die **[Fields](fields-collection-dao.md)** -Auflistung angehängt wurde, besteht Lese-/Schreibzugriff für diese Eigenschaft.

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
<td><p><strong>QueryDef-Objekt</strong></p></td>
<td><p>Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Beziehung</strong></p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Lese-/Schreibzugriff</p></td>
</tr>
</tbody>
</table>


Die Gültigkeitsprüfung wird nur für Datenbanken unterstützt, die die Microsoft Access-Datenbank-Engine verwenden.

Der von der **ValidationRule**-Eigenschaft eines **Field2**-Objekts angegebene Zeichenfolgenausdruck kann sich nur auf dieses **Field2**-Objekt beziehen. Der Ausdruck kann sich nicht auf benutzerdefinierte Funktionen, SQL-Aggregatfunktionen oder Abfragen beziehen. Damit die **ValidationRule**-Eigenschaft eines **Field2**-Objekts festgelegt werden kann, wenn die Einstellung seiner **ValidateOnSet**-Eigenschaft auf **True** festgelegt ist, muss der Ausdruck erfolgreich analysiert (wobei der Feldname ein impliziter Operand sein muss) und mit **True** ausgewertet worden sein. Ist die Einstellung seiner **ValidateOnSet**-Eigenschaft auf **False** festgelegt, wird die Einstellung der **ValidationRule**-Eigenschaft ignoriert.


> [!NOTE]
> <P>Wenn Sie die Eigenschaft auf eine Zeichenfolge mit einem nicht-Integer-Wert verkettet festlegen und die Systemparameter einer US-decimal Zeichen wie etwa ein Komma angeben (beispielsweise StrRule = "Preis &gt; " &amp; LngPrice, und LngPrice = 125,50), ein Fehler ausgegeben, wenn der Code versucht, Daten zu überprüfen. Dies ist, da während der Verkettung die Zahl in eine Zeichenfolge mit Ihr System vorgegebenen Standardzeichen für Dezimalzahlen konvertiert und Microsoft Access-Datenbankmodul SQL nur US-Dezimaltrennzeichen akzeptiert.</P>

