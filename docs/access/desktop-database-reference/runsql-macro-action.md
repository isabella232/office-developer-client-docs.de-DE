---
title: RunSQL-Makroaktion
TOCTitle: RunSQL macro action
ms:assetid: 3692142d-f8a8-e194-0b38-051167f46319
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192476(v=office.15)
ms:contentKeyID: 48544174
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12983
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: b2b745f9e58e716d4b4300034a86d87c8c7f02a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562230"
---
# <a name="runsql-macro-action"></a>RunSQL-Makroaktion

**Gilt für**: Access 2013, Office 2013

Mit der **RunSQL-Aktion** können Sie eine Access-Aktionsabfrage mithilfe der entsprechenden SQL-Anweisung ausführen. Sie können auch eine Datendefinitionsabfrage ausführen.

> [!NOTE]
> Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **AusführenSQL**-Aktion hat die folgenden Argumente.

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
<td><p><strong>SQL-Anweisung</strong></p></td>
<td><p>Die SQL-Anweisung für die Aktionsabfrage oder die Datendefinitionsabfrage, die Sie ausführen möchten. Die maximale Länge dieser Anweisung beträgt 255 Zeichen. Dies ist ein erforderliches Argument.</p></td>
</tr>
<tr class="even">
<td><p><strong>Transaktion verwenden</strong></p></td>
<td><p>Aktivieren Sie <strong>Ja</strong>, um diese Abfrage in eine Transaktion einzuschließen. Wählen Sie <strong>Nein</strong>, wenn Sie keine Transaktion verwenden möchten. Die Standardeinstellung ist <strong>Ja</strong>. Die Abfrage wird möglicherweise schneller ausgeführt, wenn Sie für dieses Argument <strong>Nein</strong> wählen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Sie können Aktionsabfragen verwenden, um Datensätze anzufügen, zu löschen und zu aktualisieren und um das Resultset einer Abfrage als neue Tabelle zu speichern. Sie können Datendefinitionsabfragen verwenden, um Tabellen oder Indizes zu erstellen, zu ändern und zu löschen. Sie können die **AusführenSQL** -Aktion verwenden, um diese Vorgänge direkt aus einem Makro heraus auszuführen, ohne gespeicherte Abfragen verwenden zu müssen.

If you need to type an SQL statement longer than 255 characters, use the **RunSQL** method of the **DoCmd** object in a Visual Basic for Applications (VBA) module instead. You can type SQL statements of up to 32,768 characters in VBA.

Access-Abfragen sind normalerweise SQL-Anweisungen, die beim Entwerfen einer Abfrage im Entwurfsbereich des Abfragefensters erstellt werden. Die folgende Tabelle enthält eine Liste der Access-Aktions- und Datendefinitionsabfragen sowie die entsprechenden SQL-Anweisungen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Abfragetyp</p></th>
<th><p>SQL-Anweisung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Aktion</strong></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Anfügen</p></td>
<td><p>INSERT INTO</p></td>
</tr>
<tr class="odd">
<td><p>Löschen</p></td>
<td><p>LÖSCHEN</p></td>
</tr>
<tr class="even">
<td><p>Make-Table</p></td>
<td><p>AUSWÄHLEN... IN</p></td>
</tr>
<tr class="odd">
<td><p>Update</p></td>
<td><p>UPDATE</p></td>
</tr>
<tr class="even">
<td><p><strong>Datendefinition (SQL-spezifisch)</strong></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Erstellen einer Tabelle</p></td>
<td><p>CREATE TABLE</p></td>
</tr>
<tr class="even">
<td><p>Ändern einer Tabelle</p></td>
<td><p>ALTER TABLE</p></td>
</tr>
<tr class="odd">
<td><p>Löschen einer Tabelle</p></td>
<td><p>DROP TABLE</p></td>
</tr>
<tr class="even">
<td><p>Erstellen eines Indexes</p></td>
<td><p>CREATE INDEX</p></td>
</tr>
<tr class="odd">
<td><p>Löschen eines Indexes</p></td>
<td><p>DROP INDEX</p></td>
</tr>
</tbody>
</table>

Zum Ändern von Daten in einer anderen Datenbank können Sie auch eine IN-Klausel mit diesen Anweisungen verwenden.

> [!NOTE]
> To run a select query or crosstab query from a macro, use the View argument of the **OpenQuery** action to open an existing select query or crosstab query in Datasheet view. You can also run existing action queries and SQL-specific queries in the same way.
