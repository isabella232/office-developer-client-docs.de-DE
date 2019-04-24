---
title: ShowAllRecords-Makroaktion
TOCTitle: ShowAllRecords macro action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 201b284a56fbd3030b41a95424b41c73ee13e385
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308645"
---
# <a name="showallrecords-macro-action"></a>ShowAllRecords-Makroaktion


**Gilt für**: Access 2013, Office 2013


Mit der **AnzeigenAlleDatensätze** -Aktion können Sie alle angewendeten Filter aus der aktiven Tabelle, dem abfrageergebnissatz oder dem Formular entfernen und alle Datensätze in der Tabelle oder im Resultset oder alle Datensätze in der zugrunde liegenden Tabelle oder Abfrage des Formulars anzeigen.

## <a name="setting"></a>Einstellung

Die **AnzeigenAlleDatensätze** -Aktion hat keine Argumente.

## <a name="remarks"></a>Bemerkungen

Mit dieser Aktion können Sie sicherstellen, dass alle Datensätze (einschließlich geänderter oder neuer Datensätze) für eine Tabelle, einen abfrageergebnissatz oder ein Formular angezeigt werden. Durch diese Aktion wird eine Neuabfrage der Datensätze für ein Formular oder ein Unterformular verursacht.

Sie können diese Aktion auch verwenden, um alle Filter zu entfernen, die mit der **ApplyFilter** -Aktion angewendet wurden, der Befehl **Filter** auf der Registerkarte **Start** oder das Argument **Filter Name** oder **Where Condition** der OpenForm-Aktion. ****

Diese Aktion hat dieselbe Wirkung wie das Klicken auf **Filter umschalten** auf der Registerkarte **Start** oder mit der rechten Maustaste auf das gefilterte Feld und das Klicken auf **Filter aus...** in der Formular-, Layout-oder Datenblattansicht.

Verwenden Sie die **AnzeigenAlleDatensätze** -Methode des **DoCmd** -Objekts, um die **ANZEIGENALLEDATENSÄTZE** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

## <a name="example"></a>Beispiel

**Anwenden eines Filters mithilfe eines Makros**

The following macro contains a set of actions, each of which filters the records for a Customer Phone List form. It shows the use of the **ApplyFilter**, **ShowAllRecords**, and **GoToControl** actions. It also shows the use of conditions to determine which toggle button in an option group has been selected on the form. Each action row is associated with a toggle button that selects the set of records starting with A, B, C, and so on, or all records. This macro should be attached to the **AfterUpdate** event of the CompanyNameFilter option group.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Bedingung</p></th>
<th><p>Aktion</p></th>
<th><p>Argumente: Einstellung</p></th>
<th><p>Kommentar</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[Company Name Filters] = 1</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Bedingung</strong>: [Firmen Name] wie &quot;[AÀÁÂÃÄ] *&quot;</p></td>
<td><p>Filtern nach Firmen, deren Name mit A, À, Á, Â, Ã oder Ä beginnt.</p></td>
</tr>
<tr class="even">
<td><p>[Company Name Filters] = 2</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Bedingung</strong>: [Firmen Name] wie &quot;B *&quot;</p></td>
<td><p>Filtern nach Firmennamen, die mit B beginnen.</p></td>
</tr>
<tr class="odd">
<td><p>[Company Name Filters] = 3</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Bedingung</strong>: [Firmen Name] wie &quot;[CÇ] *&quot;</p></td>
<td><p>Filtern nach Firmennamen, die mit C oder Ç beginnen.</p></td>
</tr>
<tr class="even">
<td><p>... Aktionszeilen für D bis Y haben dasselbe Format wie für A bis C ...</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>[Company Name Filters] = 26</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Bedingung</strong>: [Firmen Name] wie &quot;[ZÆØÅ] *&quot;</p></td>
<td><p>Filtern nach Firmennamen, die mit ZÆØ oder Å beginnen.</p></td>
</tr>
<tr class="even">
<td><p>[Company Name Filters] = 27</p></td>
<td><p><strong>ShowAllRecords</strong></p></td>
<td><p></p></td>
<td><p>Zeigt alle Datensätze an.</p></td>
</tr>
<tr class="odd">
<td><p>[RecordsetClone]. RecordCount &gt;0</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Steuerelementname</strong>: Firma</p></td>
<td><p>Verschiebt den Fokus auf das Steuerelement Firma, wenn Datensätze für den ausgewählten Buchstaben zurückgegeben werden.</p></td>
</tr>
</tbody>
</table>

