---
title: Anpassungsdatei – UserList-Abschnitt
TOCTitle: Customization File UserList section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ecaf77765051a202925449d0221f0a68a2a06622
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295156"
---
# <a name="customization-file-userlist-section"></a>Anpassungsdatei – UserList-Abschnitt


**Gilt für**: Access 2013, Office 2013

Der **userlist**-Abschnitt bezieht sich auf den **connect**-Abschnitt mit dem gleichen *identifier*-Abschnittsparameter.

Dieser Abschnitt kann einen *Benutzerzugriffs Eintrag*enthalten, der Zugriffsrechte für den angegebenen Benutzer festlegt und den *Standard* *Zugriffseintrag* im Abschnitt übereinstimmende **Verbindung** überschreibt.

## <a name="syntax"></a>Syntax

Ein Benutzerzugriffseintrag hat folgendes Format:

*Benutzername *** * = accessRights * * *

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
<td><p><em>userName</em></p></td>
<td><p>Der <em>Benutzername</em> der Person, die diese Verbindung verwendet. Gültige Benutzernamen werden mit dem Dialog <strong>Dienst-Manager</strong> von Internetinformationsdienste (Internet Information Services, IIS) eingerichtet.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>accessRights</em></strong></p></td>
<td><p>Eines der folgenden Zugriffsrechte:<br />
</p>
<ul>
<li><p><strong>NoAccess</strong> - Benutzer kann nicht auf die Datenquelle zugreifen.</p></li>
<li><p><strong>ReadOnly</strong> - Benutzer kann die Datenquelle lesen.</p></li>
<li><p><strong>ReadWrite</strong> - Benutzer kann in der Datenquelle lesen oder schreiben.</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

