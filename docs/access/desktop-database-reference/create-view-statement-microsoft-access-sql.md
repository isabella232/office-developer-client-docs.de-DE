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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706625"
---
# <a name="create-view-statement-microsoft-access-sql"></a>CREATE VIEW-Anweisung (Microsoft Access SQL)

**Betrifft**: Access 2013, Office 2013

Erstellt eine neue Sicht.

> [!NOTE]
> [!HINWEIS] Das Microsoft Access-Datenbankmodul unterstützt nicht die Verwendung der CREATE VIEW-Anweisung oder anderer DDL-Anweisungen in Kombination mit Datenbanken, die nicht aus dem Microsoft Access-Datenbankmodul stammen.

## <a name="syntax"></a>Syntax

CREATE VIEW *Sicht* \[(*Feld1*\[, *Feld2*\[,... \] \])\] AS *SELECT-Anweisung*

Die CREATE VIEW-Anweisung besteht aus folgenden Komponenten:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Komponente</p></th>
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
<td><p>Der Name des oder der Felder, die den Feldern aus der <em>Select-Anweisung</em> entsprechen.</p></td>
</tr>
<tr class="odd">
<td><p><em>SelectAnweisung</em></p></td>
<td><p>Eine SQL SELECT-Anweisung. Weitere Informationen finden Sie in der <a href="select-statement-microsoft-access-sql.md">SELECT-Anweisung</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Bei einer SELECT-Anweisung zur Definition einer Sicht kann es sich nicht um eine [SELECT INTO](select-into-statement-microsoft-access-sql.md)-Anweisung handeln.

Die SELECT-Anweisung zur Definition einer Sicht kann keine Parameter enthalten.

Der Name der Sicht darf nicht mit dem Namen einer vorhandenen Tabelle identisch sein.

Wenn die durch die SELECT-Anweisung definierte Abfrage aktualisiert werden kann, wird die Ansicht auch aktualisiert. Andernfalls ist die Sicht schreibgeschützt.

Verfügen zwei Felder in der über die SELECT-Anweisung definierten Abfrage über den gleichen Namen, muss die Definition der Sicht eine Feldliste einschließen, die für jedes der Felder in der Abfrage einen eindeutigen Namen angibt.

