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
ms.localizationpriority: medium
ms.openlocfilehash: 977fe06ce2d42616f9212fc8095ba5807aecaf86
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568936"
---
# <a name="grant-statement-microsoft-access-sql"></a>GRANT-Anweisung (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Erteilt Rechte für einen vorhandenen Benutzer oder ein vorhandene Gruppe.

## <a name="syntax"></a>Syntax

GRANT {*Berechtigung* \[ , *Berechtigung*, ... \] } ON{TABLE-Tabelle |  *OBJECT-Objekt*|

*CONTAINER-Container* } TO {*Autorisierungsname* \[ , *Autorisierungsname*, ... \] }

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
<td><p><em>Privileg</em></p></td>
<td><p>Das oder die zu erteilenden Rechte. Berechtigungen werden mit den folgenden Schlüsselwörtern angegeben: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA und UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>Tablename</em></p></td>
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

