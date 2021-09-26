---
title: BearbeitenDatensatz-Datenblock
TOCTitle: EditRecord data block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 02debed4adf3c9579b65660fcfcd27c73ed77588
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589645"
---
# <a name="editrecord-data-block"></a>BearbeitenDatensatz-Datenblock

**Gilt für**: Access 2013, Office 2013

Mit dem **BearbeitenDatensatz** -Datenblock können Sie die Werte in einem vorhandenen Datensatz ändern.

> [!NOTE]
> Der **BearbeitenDatensatz**-Datenblock ist nur in Datenmakros verfügbar.


## <a name="setting"></a>Einstellung

Der **BearbeitenDatensatz**-Datenblock kann mit den folgenden Argumenten verwendet werden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>Eine Zeichenfolge, mit der der zu bearbeitende Datensatz gekennzeichnet wird. Wenn das <em>Alias</em>-Argument nicht angegeben ist, wird der aktuelle Datensatz bearbeitet.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>HinwBemerkungeneise

Nach der **BearbeitenDatensatz** -Anweisung können Sie einen Block von Befehlen einfügen, die ausgeführt werden, bevor für die Änderungen am Datensatz ein Commit erfolgt. In einem **BearbeitenDatensatz** -Datenblock sind die folgenden Aktionen verfügbar.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="cancelrecordchange-macro-action.md">CancelRecordChange-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p><a href="comment-macro-statement.md">Kommentar-Makroanweisung</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="group-macro-statement.md">Gruppieren-Makroanweisung</a></p></td>
</tr>
<tr class="even">
<td><p><a href="if-then-else-macro-block.md">Wenn... Dann... Else-Makro-Anweisung</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="setfield-macro-action.md">SetField-Makroaktion</a></p></td>
</tr>
<tr class="even">
<td><p><a href="setlocalvar-macro-action.md">SetLocalVar-Makroaktion</a></p></td>
</tr>
</tbody>
</table>

Mit der **FestlegenFeld** -Aktion geben Sie die neuen Werte eines Felds im bearbeiteten Datensatz an.

Anschließend können Sie mit einer **Wenn...Dann...Sonst** -Anweisung Vorgänge auf der Grundlage einer Bedingung ausführen.

Wenn Sie das Bearbeiten eines Datensatzes abbrechen möchten, verwenden Sie die **AbbrechenDatensatzänderung** -Aktion. Damit verhindern Sie, dass für die Änderungen ein Commit ausgeführt wird, und der **BearbeitenDatensatz** -Datenblock wird beendet.

Über die lokale Variable **LetztesErstellenDatensatzID** in einem **DatensatzErstellen** -Datenblock können Sie mit dem zuletzt erstellten Datensatz arbeiten. Verwenden Sie beispielsweise die folgende Syntax, um auf das AssignedTo-Feld des zuletzt erstellten Datensatzes zu verweisen:

`[LastCreateRecordIdentity].[AssignedTo]`

Der DatensatzErstellen-Datenblock kann nur in den Datenmakroereignissen **[Nach Eingabe](after-insert-macro-event.md)**, **[Nach Aktualisierung](after-update-macro-event.md)** und **[Nach Aktualisierung](after-update-macro-event.md)** verwendet werden.

