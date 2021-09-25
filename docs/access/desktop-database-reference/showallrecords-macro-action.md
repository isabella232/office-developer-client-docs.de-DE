---
title: ShowAllRecords-Makroaktion
TOCTitle: ShowAllRecords macro action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a8850aa9ea4dc07abdac7e37943438be34916ffd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552514"
---
# <a name="showallrecords-macro-action"></a>ShowAllRecords-Makroaktion


**Gilt für**: Access 2013, Office 2013


Mit der **ShowAllRecords-Aktion** können Sie alle angewendeten Filter aus der aktiven Tabelle, dem Abfrageergebnissatz oder dem Formular entfernen und alle Datensätze in der Tabelle oder dem Resultset oder alle Datensätze in der dem Formular zugrunde liegenden Tabelle oder Abfrage anzeigen.

## <a name="setting"></a>Einstellung

Die **ShowAllRecords-Aktion** hat keine Argumente.

## <a name="remarks"></a>HinwBemerkungeneise

Mit dieser Aktion können Sie sicherstellen, dass alle Datensätze (einschließlich geänderter oder neuer Datensätze) für eine Tabelle, ein Abfrageergebnissatz oder ein Formular angezeigt werden. Diese Aktion bewirkt, dass die Datensätze für ein Formular oder Unterformular erneut abgefragt werden.

Sie können diese Aktion auch verwenden, um alle Filter zu entfernen, die mit der **ApplyFilter-Aktion,** dem Befehl **"Filter"** auf der Registerkarte **"Start"** oder dem Argument **"Filtername"** oder **"Bedingung"** der **OpenForm-Aktion** angewendet wurden.

Diese Aktion hat dieselbe Auswirkung wie das Klicken auf "Filter **umschalten"** auf der Registerkarte **"Start"** oder das Klicken mit der rechten Maustaste auf das gefilterte Feld und das Klicken auf **"Filter löschen"** in der Formularansicht, layoutansicht oder Datenblattansicht.

Um die **ShowAllRecords-Aktion** in einem Visual Basic for Applications (VBA)-Modul auszuführen, verwenden Sie die **ShowAllRecords-Methode** des **DoCmd-Objekts.**

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
<td><p>[Firmennamenfilter] =1</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Bedingung</strong>: [Firmenname] wie &quot; [aàáâãä]*&quot;</p></td>
<td><p>Filtern nach Firmen, deren Name mit A, À, Á, Â, Ã oder Ä beginnt.</p></td>
</tr>
<tr class="even">
<td><p>[Firmennamenfilter] =2</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Bedingung:</strong>[Firmenname] wie &quot; B*&quot;</p></td>
<td><p>Filtern nach Firmennamen, die mit B beginnen.</p></td>
</tr>
<tr class="odd">
<td><p>[Firmennamenfilter] =3</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Bedingung:</strong>[Firmenname] wie &quot; [CÇ]*&quot;</p></td>
<td><p>Filtern nach Firmennamen, die mit C oder Ç beginnen.</p></td>
</tr>
<tr class="even">
<td><p>... Aktionszeilen für D bis Y haben dasselbe Format wie für A bis C ...</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>[Firmennamenfilter] =26</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Bedingung:</strong>[Firmenname] wie &quot; [ZÆØÅ]*&quot;</p></td>
<td><p>Filtern nach Firmennamen, die mit ZÆØ oder Å beginnen.</p></td>
</tr>
<tr class="even">
<td><p>[Firmennamenfilter] =27</p></td>
<td><p><strong>ShowAllRecords</strong></p></td>
<td><p></p></td>
<td><p>Zeigt alle Datensätze an.</p></td>
</tr>
<tr class="odd">
<td><p>[RecordsetClone]. [RecordCount] &gt; 0</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Steuerelementname</strong>: Firma</p></td>
<td><p>Verschiebt den Fokus auf das Steuerelement Firma, wenn Datensätze für den ausgewählten Buchstaben zurückgegeben werden.</p></td>
</tr>
</tbody>
</table>

