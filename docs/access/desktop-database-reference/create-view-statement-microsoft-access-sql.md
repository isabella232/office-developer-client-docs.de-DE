---
title: CREATE VIEW-Anweisung (Microsoft Access SQL)
TOCTitle: CREATE VIEW Statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 292dddeab15c71fb188a928ac0e491063930214d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473810"
---
# <a name="create-view-statement-microsoft-access-sql"></a>CREATE VIEW-Anweisung (Microsoft Access SQL)


**Betrifft**: Access 2013 | Office 2013

Erstellt eine neue Sicht.


> [!NOTE]
> <P>[!HINWEIS] Das Microsoft Access-Datenbankmodul unterstützt nicht die Verwendung der CREATE VIEW-Anweisung oder anderer DDL-Anweisungen in Kombination mit Datenbanken, die nicht aus dem Microsoft Access-Datenbankmodul stammen.</P>



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
<td><p>Eine SQL-SELECT-Anweisung. Weitere Informationen finden Sie unter <a href="select-statement-microsoft-access-sql.md">SELECT-Anweisung</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Bei einer SELECT-Anweisung zur Definition einer Sicht kann es sich nicht um eine [SELECT INTO](select-into-statement-microsoft-access-sql.md)-Anweisung handeln.

Die SELECT-Anweisung zur Definition einer Sicht kann keine Parameter enthalten.

Der Name der Sicht darf nicht mit dem Namen einer vorhandenen Tabelle identisch sein.

Handelt es sich bei der über die SELECT-Anweisung definierten Abfrage, um eine Abfrage, die aktualisiert werden kann, ist die Aktualisierung der Sicht ebenfalls möglich. Andernfalls ist die Sicht schreibgeschützt.

Verfügen zwei Felder in der über die SELECT-Anweisung definierten Abfrage über den gleichen Namen, muss die Definition der Sicht eine Feldliste einschließen, die für jedes der Felder in der Abfrage einen eindeutigen Namen angibt.

