---
title: ShowAllRecords Macro Action
TOCTitle: ShowAllRecords Macro Action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 40221ce69a03f619bd15a5a89af9018c66c52791
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475616"
---
# <a name="showallrecords-macro-action"></a>ShowAllRecords Macro Action


**Betrifft**: Access 2013 | Office 2013


Sie können die **AnzeigenAlleDatensätze** -Aktion verwenden, um alle zugewiesenen Filter aus der aktiven Tabelle, Abfrage-Resultset oder Formular zu entfernen und alle Datensätze in der Tabelle oder des Resultsets oder alle Datensätze in des Formulars zugrunde liegenden Tabelle oder Abfrage anzeigen.

## <a name="setting"></a>Einstellung

Die **AnzeigenAlleDatensätze** -Aktion verfügt nicht über keine Argumente.

## <a name="remarks"></a>Hinweise

Sie können diese Aktion verwenden, um sicherzustellen, dass alle Datensätze (einschließlich aller veränderten oder neuen Datensätze) für eine Tabelle, Abfrage-Resultset oder Formular angezeigt werden. Diese Aktion bewirkt, dass eine erneute Abfrage der Datensätze in einem Formular oder Unterformular.

Sie können diese Aktion auch verwenden, um alle Filter zu entfernen, der mit der **ApplyFilter** -Aktion, dem Befehl **Filter** auf der Registerkarte **Start** **Filternamen** oder der **Where-Bedingung** -Argument der **ÖffnenFormular** -Aktion angewendet wurde.

Diese Aktion hat dieselbe Wirkung wie das durch Klicken auf der Registerkarte **Start** auf **Filter ein/aus** oder mit der rechten Maustaste des gefilterten Felds und in der Formularansicht, Entwurfsansicht oder Datenblattansicht auf **Filter löschen aus** .

Führen Sie die **AnzeigenAlleDatensätze** -Aktion in einem Visual Basic für Applikationen (VBA) Modul mit **der ShowAllRecords** -Methode des **DoCmd** -Objekts.

## <a name="example"></a>Beispiel

**Anwenden eines Filters mithilfe eines Makros**

Das folgende Makro enthält eine Reihe von Aktionen, die jeweils die Datensätze nach einem Formular Kunden-Telefonnummern filtern. Es zeigt die Verwendung der Aktionen AnwendenFilter, AnzeigenAlleDatensätze und GeheZuSteuerelement. Außerdem zeigt es die Verwendung von Bedingungen, mit denen ermittelt wird, welche Umschaltfläche in einer Optionsgruppe im Formular ausgewählt ist. Jeder Aktionszeile ist eine Umschaltfläche zugeordnet, mit der die mit A, B, C usw. beginnenden Datensatzgruppen oder alle Datensätze ausgewählt werden. Dieses Makro sollte dem AfterUpdate-Ereignis der Optionsgruppe CompanyNameFilter hinzugefügt werden.

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
<td><p>[Filter für Firma] = 1</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Bedingung</strong>: [Firma] wie &quot;[AÀÁÂÃÄ] *&quot;</p></td>
<td><p>Filtern nach Firmen, deren Name mit A, À, Á, Â, Ã oder Ä beginnt.</p></td>
</tr>
<tr class="even">
<td><p>[Filter für Firma] = 2</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Bedingung</strong>: [Firma] wie &quot;B *&quot;</p></td>
<td><p>Filtern nach Firmennamen, die mit B beginnen.</p></td>
</tr>
<tr class="odd">
<td><p>[Filter für Firma] = 3</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Bedingung</strong>: [Firma] wie &quot;[CÇ] *&quot;</p></td>
<td><p>Filtern nach Firmennamen, die mit C oder Ç beginnen.</p></td>
</tr>
<tr class="even">
<td><p>... Aktionszeilen für D bis Y haben dasselbe Format wie für A bis C ...</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>[Filter für Firma] = 26</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Bedingung</strong>: [Firma] wie &quot;[ZÆØÅ] *&quot;</p></td>
<td><p>Filtern nach Firmennamen, die mit ZÆØ oder Å beginnen.</p></td>
</tr>
<tr class="even">
<td><p>[Filter für Firma] = 27</p></td>
<td><p><strong>ShowAllRecords</strong></p></td>
<td><p></p></td>
<td><p>Zeigt alle Datensätze an.</p></td>
</tr>
<tr class="odd">
<td><p>[RecordsetClone]. [RecordCount] &gt;0</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Steuerelementname</strong>: Firma</p></td>
<td><p>Verschiebt den Fokus auf das Steuerelement Firma, wenn Datensätze für den ausgewählten Buchstaben zurückgegeben werden.</p></td>
</tr>
</tbody>
</table>

