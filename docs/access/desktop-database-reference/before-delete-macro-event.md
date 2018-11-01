---
title: Makroereignis 'Vor Löschung'
TOCTitle: Before Delete Macro Event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0ee4878a742454eb1b02f4b9a45c14ad79097c46
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876260"
---
# <a name="before-delete-macro-event"></a>Makroereignis "Vor Löschung"

**Betrifft**: Access 2013, Office 2013

Das Ereignis **Vor Löschung** tritt ein, wenn ein Datensatz gelöscht wird, jedoch bevor der Commit für die Änderung erfolgt ist.

> [!NOTE]
> [!HINWEIS] Das Ereignis **Vor Löschung** ist nur in Datenmakros verfügbar.

## <a name="remarks"></a>Hinweise

Mit dem Ereignis **Vor Löschung** führen Sie sämtliche Aktionen vor dem Löschen eines Datensatzes aus. Das Ereignis **Vor Änderung** wird häufig verwendet, um Überprüfungen auszuführen und benutzerdefinierte Fehlermeldungen auszugeben.

Sie können einen Wert in den Datensatz gelöscht wird, mithilfe der folgenden Syntax zugreifen:

`[Old].[Field Name]`

Um den Wert des QuantityInStock-Felds im zu löschenden Datensatz zugreifen möchten, verwenden Sie beispielsweise die folgende Syntax:

`[Old].[QuantityInStock]`

Am Ende des Ereignisses **Vor Löschung** werden die Werte im zu löschenden Datensatz dauerhaft gelöscht.

Sie können das Ereignis **Vor Löschung** mit der **Auslösenfehler** -Aktion abbrechen. Wenn ein Fehler ausgelöst wird, werden die Änderungen, die im Ereignis **Vor Löschung** enthaltenen verworfen.

In der folgenden Tabelle sind Makros ausgeführt, die im Ereignis **Vor Löschung** verwendet werden können.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Befehlstyp</p></th>
<th><p>Command</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Programmablauf</p></td>
<td><p><a href="comment-macro-statement.md">Kommentar-Makroanweisung</a></p></td>
</tr>
<tr class="even">
<td><p>Programmablauf</p></td>
<td><p><a href="group-macro-statement.md">Gruppieren-Makroanweisung</a></p></td>
</tr>
<tr class="odd">
<td><p>Programmablauf</p></td>
<td><p><a href="if-then-else-macro-block.md">If... Im Anschluss: Makroblock</a></p></td>
</tr>
<tr class="even">
<td><p>Datenblock</p></td>
<td><p><a href="lookuprecord-data-block.md">NachschlagenDatensatz-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Löschenmakrofehler-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="onerror-macro-action.md">BeiFehler-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="raiseerror-macro-action.md">Auslösenfehler-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p>Datenaktion</p></td>
<td><p><a href="setlocalvar-macro-action.md">FestlegenLokaleVar-Makroaktion</a></p></td>
</tr>
<tr class="odd">
<td><p>Datenaktion</p></td>
<td><p><a href="stopmacro-macro-action.md">StoppMakro-Makroaktion</a></p></td>
</tr>
</tbody>
</table>


Zum Erstellen eines Datenmakros, mit dem das Ereignis **Vor Löschung** erfasst wird, führen Sie die folgenden Schritte aus.

1.  Öffnen Sie die Tabelle, für die Sie das Ereignis **Vor Löschung** erfassen möchten.

2.  Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Vorabereignisse** wählen Sie **Vor dem Löschen**.

