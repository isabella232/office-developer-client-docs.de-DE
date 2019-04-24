---
title: TableDef. ValidationRule-Eigenschaft (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 7dcd6f2c-45bc-a50b-727d-589371d5803f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196425(v=office.15)
ms:contentKeyID: 48545864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052925
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 44329a4cc320e9adcc0612629bcc3fdcd179a1c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314882"
---
# <a name="tabledefvalidationrule-property-dao"></a>TableDef. ValidationRule-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Legt einen Wert fest, der die Daten in einem Feld überprüft, wenn es geändert oder einer Tabelle hinzugefügt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . ValidationRule

*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung bzw. der Rückgabewert ist ein **String**-Wert, der einen Vergleich in der Form einer SQL WHERE-Klausel ohne das reservierte Wort WHERE beschreibt. Für ein Objekt, das noch nicht an die **Fields**-Auflistung angehängt wurde, besteht Lese-/Schreibzugriff für diese Eigenschaft.

Die **ValidationRule**-Eigenschaft legt fest, ob ein Feld gültige Daten enthält. Wenn die Daten nicht gültig sind, tritt ein auffangbarer Laufzeitfehler auf. Die zurückgegebene Fehlermeldung ist der Text der **ValidationText**-Eigenschaft, sofern er festgelegt wurde, oder der Text des Ausdrucks aus **ValidationRule**.

Die Gültigkeitsprüfung wird nur für Datenbanken unterstützt, die die Microsoft Access-Datenbank-Engine verwenden.

Der von der **ValidationRule**-Eigenschaft eines **Field**-Objekts festgelegte Zeichenfolgenausdruck kann sich nur auf das betreffende **Field**-Objekt beziehen. Der Ausdruck kann sich nicht auf benutzerdefinierte Funktionen, SQL-Aggregatfunktionen oder Abfragen beziehen. Um die **ValidationRule**-Eigenschaft eines **Field**-Objekts festzulegen, wenn seine **ValidateOnSet**-Eigenschaft den Wert **True** hat, muss der Ausdruck erfolgreich analysiert werden (mit dem Feldnamen als impliziter Operand) und den Wert **True** ergeben. Wenn die **ValidateOnSet**-Eigenschaft des Objekts den Wert **False** hat, wird die **ValidationRule**-Einstellung ignoriert.

Die **ValidationRule**-Eigenschaft eines **Recordset**- oder **TableDef**-Objekts kann sich auf mehrere Felder in diesem Objekt beziehen. Es gelten die weiter oben in diesem Thema genannten Einschränkungen für das **Field**-Objekt.

Bei einem **TableDef**-Objekt, das auf einer verknüpften Tabelle basiert, erbt die **ValidationRule**-Eigenschaft den Wert der **ValidationRule**-Eigenschaft der zugrunde liegenden Basistabelle. Wenn die zugrunde liegende Basistabelle keine Gültigkeitsprüfung unterstützt, ist der Wert dieser Eigenschaft eine leere Zeichenfolge ("").

> [!NOTE]
> Wenn Sie die-Eigenschaft auf eine Zeichenfolge festlegen, die mit einem nicht-ganzzahligen Wert verkettet ist, und die Systemparameter ein nicht-U. S. Decimal-Zeichen wie ein Komma (beispielsweise strRule &gt; = &amp; "Price" lngPrice und lngPrice = 125, 50) angeben, tritt ein Fehler auf, wenn Ihr Code versucht, alle Daten zu überprüfen. Dies liegt daran, dass der Wert während der Verkettung mithilfe des Standard-Dezimaltrennzeichens in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-Dezimaltrennzeichen akzeptiert.
