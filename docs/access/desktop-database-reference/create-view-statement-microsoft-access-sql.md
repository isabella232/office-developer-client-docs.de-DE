---
title: CREATE VIEW-Anweisung (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 2f46b897ba4e37f454c656f39333f5c4e0389e94
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581588"
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

Wenn die durch die SELECT-Anweisung definierte Abfrage aktualisierbar ist, ist auch die Ansicht aktualisierbar. Andernfalls ist die Ansicht schreibgeschützt.

Wenn zwei beliebige Felder in der durch die SELECT-Anweisung definierten Abfrage denselben Namen haben, muss die Sichtdefinition eine Feldliste mit eindeutigen Namen für jedes Feld in der Abfrage enthalten.

