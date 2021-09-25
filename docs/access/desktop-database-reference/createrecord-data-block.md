---
title: Datensatzerstellen-Datenblock erstellen
TOCTitle: CreateRecord data block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2430e3731f83c59eb039f504609772cdc69b9695
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581595"
---
# <a name="createrecord-data-block"></a>Datensatzerstellen-Datenblock erstellen


**Gilt für**: Access 2013, Office 2013

Mit dem **DatensatzErstellen**-Datenblock können Sie einen neuen Datensatz in der angegebenen Tabelle erstellen.

> [!NOTE]
> Der **DatensatzErstellen**-Datenblock ist nur in Datenmakros verfügbar.

## <a name="setting"></a>Einstellung

Der **DatensatzErstellen**-Datenblock kann mit den folgenden Argumenten verwendet werden.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Erforderlich</p></th>
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


## <a name="remarks"></a>HinwBemerkungeneise

Der mit **DatensatzErstellen** erstellte Datensatz wird automatisch als aktueller Datensatz festgelegt.

Nach **der CreateRecord-Anweisung** können Sie einen Befehlsblock einfügen, der ausgeführt wird, bevor für den neuen Datensatz ein Commit ausgeführt wird. In einem **DatensatzErstellen**-Datenblock sind die folgenden Aktionen verfügbar.

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


Wenn mit der **DatensatzErstellen** -Aktion ein Datensatz erstellt wurde, geben Sie mit der **FestlegenFeld** -Aktion den Wert eines Felds im neuen Datensatz an.

Anschließend können Sie mit einer **Wenn...Dann...Sonst** -Anweisung Vorgänge auf der Grundlage einer Bedingung ausführen.

Wenn Sie das Erstellen eines Datensatzes abbrechen möchten, verwenden Sie die **AbbrechenDatensatzänderung** -Aktion. Damit verhindern Sie, dass für die Änderungen ein Commit ausgeführt wird, und der **DatensatzErstellen** -Datenblock wird beendet.

Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record. Verwenden Sie beispielsweise die folgende Syntax, um auf das Feld AssignedTo des zuletzt erstellten Datensatzes zu verweisen.

`[LastCreateRecordIdentity].[AssignedTo]`

Der **DatensatzErstellen** -Datenblock kann nur in den Datenmakroereignissen **[Nach Eingabe](after-insert-macro-event.md)**, **[Nach Aktualisierung](after-update-macro-event.md)** und **[Nach Aktualisierung](after-update-macro-event.md)** verwendet werden.

