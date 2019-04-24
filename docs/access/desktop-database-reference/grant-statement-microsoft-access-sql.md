---
title: GRANT-Anweisung (Microsoft Access SQL)
TOCTitle: GRANT statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4357099f8bcb9b2308b5cda3543949765b8c3420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292132"
---
# <a name="grant-statement-microsoft-access-sql"></a>GRANT-Anweisung (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Erteilt Rechte für einen vorhandenen Benutzer oder ein vorhandene Gruppe.

## <a name="syntax"></a>Syntax

Grant {*Berechtigung*\[, *Privileg*,... \]} On {Table *Tabelle* | Objekt *Objekt*|

Container *Container* } an {*authorizationname*\[, *authorizationname*,... \]}

Die GRANT-Anweisung besteht aus folgenden Komponenten:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Teil</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Berechtigungen</em></p></td>
<td><p>Das oder die zu erteilenden Rechte. Berechtigungen werden mithilfe der folgenden Schlüsselwörter angegeben: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, dbPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA und UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>TableName</em></p></td>
<td><p>Ein gültiger Tabellenname.</p></td>
</tr>
<tr class="odd">
<td><p><em>object</em></p></td>
<td><p>Ein Objekt kann jedes Objekt umfassen, bei dem es sich nicht um eine Tabelle handelt. Beispiele für solche Objekte sind gespeicherte Abfragen, Sichten oder Prozeduren.</p></td>
</tr>
<tr class="even">
<td><p><em>Container</em></p></td>
<td><p>Der Name eines gültigen Containers.</p></td>
</tr>
<tr class="odd">
<td><p><em>Autorisierungsname</em></p></td>
<td><p>Der Name eines Benutzers oder einer Gruppe.</p></td>
</tr>
</tbody>
</table>

