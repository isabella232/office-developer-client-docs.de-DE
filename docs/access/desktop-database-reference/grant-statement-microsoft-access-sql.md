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
ms.openlocfilehash: 4e37c0853c2b80c42bb2560cb0a19122c45f85f4
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860876"
---
# <a name="grant-statement-microsoft-access-sql"></a>GRANT-Anweisung (Microsoft Access SQL)

**Betrifft**: Access 2013 | Office 2013

Erteilt Rechte für einen vorhandenen Benutzer oder ein vorhandene Gruppe.

## <a name="syntax"></a>Syntax

GRANT {*Recht*\[, *Berechtigung*,... \]} ON {Tabelle *Tabelle* | OBJECT- *Objekt*|

CONTAINER *Container* } TO {*autorisierungsname*\[, *autorisierungsname*,... \]}

Die GRANT-Anweisung besteht aus folgenden Komponenten:

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
<td><p><em>Berechtigung</em></p></td>
<td><p>Der geringsten Rechte oder Berechtigungen erteilt werden. Berechtigungen werden mithilfe der folgenden Schlüsselwörter angegeben: auswählen, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, erstellen, SELECTSCHEMA, SCHEMA und UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>Tabellenname</em></p></td>
<td><p>Ein gültiger Tabellenname.</p></td>
</tr>
<tr class="odd">
<td><p><em>Objekt</em></p></td>
<td><p>Dies kann jedes Objekt sein, das nicht aus einer Tabelle stammt. Ein Beispiel ist eine gespeicherte Abfrage (Sicht oder Prozedur).</p></td>
</tr>
<tr class="even">
<td><p><em>Container</em></p></td>
<td><p>Der Name eines gültigen Containers.</p></td>
</tr>
<tr class="odd">
<td><p><em>Autorisierungsname</em></p></td>
<td><p>Ein Benutzer- oder Gruppenname.</p></td>
</tr>
</tbody>
</table>

