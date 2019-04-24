---
title: Recordset2. ValidationRule-Eigenschaft (DAO)
TOCTitle: ValidationRule Property
ms:assetid: d46cc255-e588-e9e6-66d7-31fc26ae45b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835002(v=office.15)
ms:contentKeyID: 48547940
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7b146aa0278db278f3831bc0e00987d21e14b70a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307154"
---
# <a name="recordset2validationrule-property-dao"></a>Recordset2. ValidationRule-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Legt einen Wert fest, der die Daten in einem Feld überprüft, wenn es geändert oder einer Tabelle hinzugefügt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . ValidationRule

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung bzw. der Rückgabewert ist ein **String**-Wert, der einen Vergleich in der Form einer SQL WHERE-Klausel ohne das reservierte Wort WHERE beschreibt. Für ein Objekt, das noch nicht an die **Fields**-Auflistung angehängt wurde, besteht Lese-/Schreibzugriff für diese Eigenschaft.

Die **ValidationRule**-Eigenschaft legt fest, ob ein Feld gültige Daten enthält. Wenn die Daten nicht gültig sind, tritt ein auffangbarer Laufzeitfehler auf. Die zurückgegebene Fehlermeldung ist der Text der **ValidationText**-Eigenschaft, sofern er festgelegt wurde, oder der Text des Ausdrucks aus **ValidationRule**.

Für ein **Recordset**-Objekt ist die **ValidationRule**-Eigenschaft schreibgeschützt. Für ein **TableDef**-Objekt hängt die Verwendung der **ValidationRule**-Eigenschaft vom Status des **TableDef**-Objekts ab, wie in der folgenden Tabelle dargestellt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>TableDef</p></th>
<th><p>Verwendung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Basistabelle</p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="even">
<td><p>Verknüpfte Tabelle</p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
</tbody>
</table>


Die Gültigkeitsprüfung wird nur für Datenbanken unterstützt, die die Microsoft Access-Datenbank-Engine verwenden.

Der von der **ValidationRule**-Eigenschaft eines **Field**-Objekts festgelegte Zeichenfolgenausdruck kann sich nur auf das betreffende **Field**-Objekt beziehen. Der Ausdruck kann sich nicht auf benutzerdefinierte Funktionen, SQL-Aggregatfunktionen oder Abfragen beziehen. Um die **ValidationRule**-Eigenschaft eines **Field**-Objekts festzulegen, wenn seine **ValidateOnSet**-Eigenschaft den Wert **True** hat, muss der Ausdruck erfolgreich analysiert werden (mit dem Feldnamen als impliziter Operand) und den Wert **True** ergeben. Wenn die **ValidateOnSet**-Eigenschaft des Objekts den Wert **False** hat, wird die **ValidationRule**-Einstellung ignoriert.

Die **ValidationRule**-Eigenschaft eines **Recordset**- oder **TableDef**-Objekts kann sich auf mehrere Felder in diesem Objekt beziehen. Es gelten die weiter oben in diesem Thema genannten Einschränkungen für das **Field**-Objekt.

For a table-type **Recordset** object, the **ValidationRule** property inherits the **ValidationRule** property setting of the **TableDef** object that you use to create the table-type **Recordset** object.

> [!NOTE]
> Wenn Sie die-Eigenschaft auf eine Zeichenfolge festlegen, die mit einem nicht-ganzzahligen Wert verkettet ist, und die Systemparameter ein nicht-U. S. Decimal-Zeichen wie ein Komma (beispielsweise strRule &gt; = &amp; "Price" lngPrice und lngPrice = 125, 50) angeben, tritt ein Fehler auf, wenn Ihr Code versucht, alle Daten zu überprüfen. Dies liegt daran, dass der Wert während der Verkettung mithilfe des Standard-Dezimaltrennzeichens in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-Dezimaltrennzeichen akzeptiert.</P>

