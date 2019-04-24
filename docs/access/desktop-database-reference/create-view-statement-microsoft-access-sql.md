---
title: CREATE VIEW-Anweisung (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 73fac5ff9dd1f5cf277b8cb241044af23609b764
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295366"
---
# <a name="create-view-statement-microsoft-access-sql"></a>CREATE VIEW-Anweisung (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Erstellt eine neue Sicht.

> [!NOTE]
> Das Microsoft Access-Datenbankmodul unterstützt nicht die Verwendung von CREATE VIEW oder einer der DDL-Anweisungen für Datenbanken, die nicht mit dem Microsoft Access-Datenbankmodul erstellt wurden.

## <a name="syntax"></a>Syntax

CREATE VIEW *view* \[(*field1*\[, *field2*\[, …\]\])\] AS *selectstatement*

Die CREATE VIEW-Anweisung setzt sich wie folgt zusammen:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Part</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>view</em></p></td>
<td><p>Der Name der zu erstellenden Sicht.</p></td>
</tr>
<tr class="even">
<td><p><em>Feld1</em>, <em>Feld2</em></p></td>
<td><p>Die Namen der Felder für die entsprechenden in der <em>SELECT-Anweisung</em> angegebenen Felder.</p></td>
</tr>
<tr class="odd">
<td><p><em>SELECT-Anweisung</em></p></td>
<td><p>Eine SQL SELECT-Anweisung. Weitere Informationen finden Sie unter <a href="select-statement-microsoft-access-sql.md">SELECT-Anweisung</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Bei einer SELECT-Anweisung zur Definition einer Sicht kann es sich nicht um eine [SELECT INTO](select-into-statement-microsoft-access-sql.md)-Anweisung handeln.

Die SELECT-Anweisung, die die Sicht definiert, darf keine Parameter enthalten.

Der Name der Sicht darf nicht mit dem Namen einer vorhandenen Tabelle übereinstimmen.

Handelt es sich bei der über die SELECT-Anweisung definierten Abfrage um eine Abfrage, die aktualisiert werden kann, ist die Aktualisierung der Sicht ebenfalls möglich. Andernfalls ist die Sicht schreibgeschützt.

Wenn zwei beliebige Felder in der durch die SELECT-Anweisung definierten Abfrage denselben Namen haben, muss die Sichtdefinition eine Feldliste mit eindeutigen Namen für jedes Feld in der Abfrage enthalten.

