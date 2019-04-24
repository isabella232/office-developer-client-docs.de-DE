---
title: REVOKE-Anweisung (Microsoft Access SQL)
TOCTitle: REVOKE statement (Microsoft Access SQL)
ms:assetid: 69399fd6-c4e8-f2e2-e5f4-48ae779323f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195272(v=office.15)
ms:contentKeyID: 48545409
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277479
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 20122fee617597987940766a076d5f968a87c2d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306531"
---
# <a name="revoke-statement-microsoft-access-sql"></a>REVOKE-Anweisung (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Widerruft bestimmte Berechtigungen eines vorhandenen Benutzers oder einer Gruppe.

## <a name="syntax"></a>Syntax

REVOKE {*Privilege*\[, *Privileg*,... \]} On {Table *Tabelle* | Objekt *Objekt*|

*Container*für "beflecker"**\[von {authorizationname, *authorizationname*,... \]}

Die REVOKE-Anweisung enthält folgende Bestandteile:

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
<td><p>Die zu widerrufenden Berechtigungen. Berechtigungen werden mithilfe der folgenden Schlüsselwörter angegeben: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, dbPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA und UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>table</em></p></td>
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

