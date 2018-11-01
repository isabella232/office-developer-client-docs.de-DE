---
title: FestlegenSortiertNach-Makroaktion
TOCTitle: SetOrderBy Macro Action
ms:assetid: 78f65ce9-b56f-f476-3bd6-f3307bc22a08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196152(v=office.15)
ms:contentKeyID: 48545765
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98639
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ac911110d313243879d6dff993061d58c208cd34
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876218"
---
# <a name="setorderby-macro-action"></a>FestlegenSortiertNach-Makroaktion


**Betrifft**: Access 2013, Office 2013

Mit der **FestlegenSortiertNach** -Aktion legen Sie fest, wie die Datensätze in einem Formular, einem Bericht, einer Tabelle oder einem Abfrageergebnis sortiert werden sollen.

## <a name="setting"></a>Einstellung

Die **FestlegenSortiertNach** -Aktion kann mit den folgenden Argumenten verwendet werden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktionsargument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Sortiert nach</strong></p></td>
<td><p>Ein Zeichenfolgenausdruck, der den Namen des Felds oder der Felder, nach dem oder denen Datensätze sortiert werden sollen, sowie die optionalen ASC- oder DESC-Schlüsselwörter enthält.</p></td>
</tr>
<tr class="even">
<td><p><strong>Steuerelementname</strong></p></td>
<td><p>Wenn das Argument angegeben ist und es sich beim aktiven Objekt um ein Formular oder einen Bericht handelt, der Name des Steuerelements, das dem zu sortierenden Unterformular oder Unterbericht entspricht. Wenn das Argument leer ist und es sich beim aktiven Objekt um ein Formular oder einen Bericht handelt, wird das übergeordnete Formular bzw. der übergeordnete Bericht sortiert.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Beim Ausführen dieser Makroaktion wird die Sortierung auf die Tabelle, das Formular, den Bericht oder das Datenblatt (Abfrageergebnis) angewendet, das aktiv ist und den Fokus besitzt.

Das Argument Sortiert nach bildet den Namen des Felds oder der Felder, nach dem oder denen Sie Datensätze sortieren möchten. Wenn Sie mehr als einen Feldnamen verwenden, trennen Sie die Namen durch ein Komma (,). Die **SortiertNach** -Eigenschaft des aktiven Objekts wird verwendet, um einen Sortierwert zu speichern, den Sie später anwenden können. SortiertNach-Werte werden mit den Objekten gespeichert, in denen sie erstellt werden. Sie werden automatisch geladen, wenn das Objekt geöffnet wird, jedoch nicht automatisch angewendet.

Wenn Sie das Argument Sortiert nach durch Eingeben eines oder mehrerer Feldnamen festlegen und anschließend das Makro ausführen, werden die Datensätze standardmäßig in aufsteigender Reihenfolge sortiert.

Wenn Sie Datensätze in absteigender Reihenfolge sortieren möchten, geben Sie am Ende des Argumentausdrucks „Sortiert nach" die Zeichenfolge „DESC" ein. Wenn Sie beispielsweise Kundendatensätze in absteigender Reihenfolge nach Kontaktnamen sortieren möchten, legen Sie das Argument „Sortiert nach" auf „Kontaktperson DESC" fest. Wenn Sie Namen in absteigender Reihenfolge nach Nachname und in aufsteigender Reihenfolge nach Vorname sortieren möchten, legen Sie das Argument „Sortiert nach" auf „Nachname DESC, Vorname ASC" fest.

