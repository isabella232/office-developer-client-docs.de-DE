---
title: DatensatzErstellen-Datenblock
TOCTitle: CreateRecord Data Block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62c6902cc57c210d617b71da3ca42a2a52bdd4f6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474106"
---
# <a name="createrecord-data-block"></a>DatensatzErstellen-Datenblock


**Betrifft**: Access 2013 | Office 2013

Mit dem **DatensatzErstellen** -Datenblock können Sie einen neuen Datensatz in der angegebenen Tabelle erstellen.

> [!NOTE]
> [!HINWEIS] Der **DatensatzErstellen** -Datenblock ist nur in Datenmakros verfügbar.

## <a name="setting"></a>Einstellung

Der **DatensatzLöschen** -Datenblock kann mit den folgenden Argumenten verwendet werden.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Eingabe erforderlich</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Datensatz erstellen in</strong></p></td>
<td><p>Ja</p></td>
<td><p>Der Name der Tabelle, in der der neue Datensatz erstellt werden soll</p></td>
</tr>
<tr class="even">
<td><p><strong>Alias</strong></p></td>
<td><p>Nein</p></td>
<td><p>Eine Zeichenfolge zur Kennzeichnung des Datensatzes Sie können den Alias des Datensatzes zur Kennzeichnung verwenden</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Der mit **DatensatzErstellen** erstellte Datensatz wird automatisch als aktueller Datensatz festgelegt.

Nach der **DatensatzErstellen** -Anweisung können Sie einen Block von Befehlen einfügen, die ausgeführt wird, bevor ein Commit für der neue Datensatz ausgeführt wird. In einem **DatensatzErstellen** -Datenblock sind die folgenden Aktionen verfügbar.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="cancelrecordchange-macro-action.md">AbbrechenDatensatzänderung-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p><a href="comment-macro-statement.md">Kommentar-Makroanweisung</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="group-macro-statement.md">Gruppieren-Makroanweisung</a></p></td>
</tr>
<tr class="even">
<td><p><a href="if-then-else-macro-block.md">If... Im Anschluss: Else-Makroanweisung</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="setfield-macro-action.md">FestlegenFeld-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p><a href="setlocalvar-macro-action.md">FestlegenLokaleVar-Makroaktion</a></p></td>
</tr>
</tbody>
</table>


Wenn mit der **DatensatzErstellen** -Aktion ein Datensatz erstellt wurde, geben Sie mit der **FestlegenFeld** -Aktion den Wert eines Felds im neuen Datensatz an.

Anschließend können Sie mit einer **Wenn...Dann...Sonst** -Anweisung Vorgänge auf der Grundlage einer Bedingung ausführen.

Wenn Sie das Erstellen eines Datensatzes abbrechen möchten, verwenden Sie die **AbbrechenDatensatzänderung** -Aktion. Damit verhindern Sie, dass für die Änderungen ein Commit ausgeführt wird, und der **DatensatzErstellen** -Datenblock wird beendet.

Nachdem der neue Datensatz ein Commit ausgeführt wird, können Sie die lokale Variable **LastCreateRecordIdentity** den Eintrag entwickelt verwenden. Verwenden Sie beispielsweise die folgende Syntax, um des Felds AssignedTo die zuletzt erstellte Datensatz zu verweisen.

`[LastCreateRecordIdentity].[AssignedTo]`

Der **DatensatzErstellen** -Datenblock kann nur in den Datenmakroereignissen **[Nach Eingabe](after-insert-macro-event.md)**, **[Nach Aktualisierung](after-update-macro-event.md)** und **[Nach Aktualisierung](after-update-macro-event.md)** verwendet werden.

