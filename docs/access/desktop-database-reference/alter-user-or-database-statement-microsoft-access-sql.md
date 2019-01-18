---
title: ALTER USER- oder DATABASE-Anweisung (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2514ca6403ce70acae9e344d610fbd7b9ba7d73b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702285"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a>ALTER USER- oder DATABASE-Anweisung (Microsoft Access SQL)

**Betrifft**: Access 2013, Office 2013

Ändert das Kennwort für einen vorhandenen Benutzer oder eine Datenbank.

## <a name="syntax"></a>Syntax

ALTER DATABASE PASSWORD *neuesKennwort altesKennwort*

ALTER USER *Benutzer* PASSWORD *neuesKennwort altesKennwort*

Die ALTER USER- oder DATABASE-Anweisung besteht aus den folgenden Komponenten:

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
<td><p><em>Benutzer</em></p></td>
<td><p>Der Name eines Benutzers, der der Arbeitsgruppen-Informationsdatei hinzugefügt werden soll.</p></td>
</tr>
<tr class="even">
<td><p><em>NeuesKennwort</em></p></td>
<td><p>Das neue Kennwort, das dem <em>Benutzer</em> oder der <em>Datenbank</em> zugeordnet werden soll.</p></td>
</tr>
<tr class="odd">
<td><p><em>AltesKennwort</em></p></td>
<td><p>Das bestehende Kennwort, das dem angegebenen <em>Benutzer</em> oder der angegebenen <em>Gruppe</em> zugeordnet ist.</p></td>
</tr>
</tbody>
</table>

