---
title: Recordset. RecordsetType-Eigenschaft (DAO)
TOCTitle: RecordsetType Property
ms:assetid: a66d4043-08cc-ead1-f9ff-efc7d7ea21bf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821178(v=office.15)
ms:contentKeyID: 48546853
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13361
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 64f7dda8bec7806ef510d265deab350dc3cdad6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307630"
---
# <a name="recordsetrecordsettype-property-dao"></a>Recordset. RecordsetType-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Sie können mit der **RecordsetType**-Eigenschaft angeben, welche Art von Recordset für ein Formular bereit gestellt wird. **Byte**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . RecordsetType

*expression* Eine Variable, die ein **Form**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die **RecordsetType**-Eigenschaft verwendet die folgenden Einstellungen in einer Microsoft Access-Datenbank.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Einstellung</p></th>
<th><p>Recordset-Typ</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0</p></td>
<td><p>Dynaset</p></td>
<td><p>(Standardeinstellung) Sie können gebundene Steuerelemente auf der Basis einer einzigen Tabelle oder von Tabellen mit einer 1:1-Beziehung bearbeiten. Für Steuerelemente, die an Felder gebunden sind, die auf Tabellen mit einer 1: n-Beziehung basieren, können Sie Daten aus dem &quot;Join&quot; -Feld auf der 1-Seite der Beziehung nur bearbeiten, wenn die Cascade-Aktualisierung zwischen den Tabellen aktiviert ist.</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td><p>Dynaset (Unregelmäßige Aktualisierungen)</p></td>
<td><p>Alle Tabellen und an ihre Felder gebundenen Steuerelemente können bearbeitet werden.</p></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
<td><p>Snapshot</p></td>
<td><p>Es können keine Tabellen oder an ihre Felder gebundenen Steuerelemente bearbeitet werden.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Wenn Sie vermeiden möchten, dass Daten in gebundenen Steuerelementen bearbeitet werden, wenn das Formular in der Formularansicht oder Datenblattansicht angezeigt wird, können Sie die **RecordsetType**-Eigenschaft auf 2 festlegen.

Die **RecordsetType**-Eigenschaft verwendet die folgenden Einstellungen in einem Microsoft Access-Projekt (ADP).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Einstellung</p></th>
<th><p>Recordset-Typ</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>3</p></td>
<td><p>Snapshot</p></td>
<td><p>Es können keine Tabellen oder an ihre Felder gebundenen Steuerelemente bearbeitet werden.</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p>Aktualisierbarer Snapshot</p></td>
<td><p>(Standardeinstellung) Alle Tabellen und an ihre Felder gebundenen Steuerelemente können bearbeitet werden.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Wenn die **RecordsetType**-Eigenschaft eines geöffneten Formulars oder Berichts geändert wird, führt dies zu einer automatischen Neuerstellung der Datensatzgruppe.

Sie können Formulare erstellen, die auf mehreren zugrunde liegenden Tabellen basieren, an deren Felder Steuerelemente in den Formularen gebunden sind. Abhängig von der Einstellung der **RecordsetType** -Eigenschaft können Sie einschränken, welche gebundenen Steuerelemente bearbeitet werden können.

Zusätzlich zu dem von der **RecordsetType** -Eigenschaft bereitgestellten Bearbeitungssteuerelement verfügt jedes Steuerelement in einem Formular über eine **Locked** -Eigenschaft, mit der Sie angeben können, ob das Steuerelement und die ihm zugrunde liegenden Daten bearbeitet werden können. Ist die **Locked** -Eigenschaft auf Ja festgelegt, können die Daten nicht bearbeitet werden.

## <a name="example"></a>Beispiel

Im folgenden Beispiel können Datensätze nur dann aktualisiert werden, wenn die Benutzer-ID ADMIN lautet. In diesem Codebeispiel wird die **RecordsetType**-Eigenschaft auf Snapshot festgelegt, wenn die öffentliche Variable gstrUserID nicht den Wert ADMIN hat.

```vb
    Sub Form_Open(Cancel As Integer) 
     Const conSnapshot = 2 
     If gstrUserID <> "ADMIN" Then 
     Forms!Employees.RecordsetType = conSnapshot 
     End If 
    End Sub
```

## <a name="see-also"></a>Siehe auch

- [Form-Objekt](https://docs.microsoft.com/office/vba/api/Access.Form)


