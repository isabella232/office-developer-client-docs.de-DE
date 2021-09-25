---
title: Recordset.ValidationRule-Eigenschaft (DAO)
TOCTitle: ValidationRule Property
ms:assetid: c9250c13-18fe-1ff7-7846-7872c49a1e3b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823208(v=office.15)
ms:contentKeyID: 48547671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: dd54fa6b9c8aca40b16185b51dc43adce785c87b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606065"
---
# <a name="recordsetvalidationrule-property-dao"></a>Recordset.ValidationRule-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Legt einen Wert fest, der die Daten in einem Feld überprüft, wenn es geändert oder einer Tabelle hinzugefügt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . Validationrule

*Ausdruck* Eine Variable, die ein **Recordset**-Objekt darstellt.

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
<th><p>Nutzung</p></th>
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
> Wenn Sie die Eigenschaft auf eine Zeichenfolge festlegen, die mit einem Nicht-Ganzzahlwert verkettet ist, und die Systemparameter eine Nicht-USA angeben. Dezimalzeichen wie z. B. ein Komma (z. B. strRule = "PRICE &gt; " &amp; lngPrice und gifPrice = 125,50) führt zu einem Fehler, wenn Ihr Code versucht, Daten zu überprüfen. Dies liegt daran, dass der Wert während der Verkettung mithilfe des Standard-Dezimaltrennzeichens in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-Dezimaltrennzeichen akzeptiert.
