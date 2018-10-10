---
title: UserList-Abschnitt der Anpassungsdatei
TOCTitle: Customization File UserList Section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a14060858ad5cd90b410319a515eb271b2b397ea
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474788"
---
# <a name="customization-file-userlist-section"></a>UserList-Abschnitt der Anpassungsdatei


**Betrifft**: Access 2013 | Office 2013

Der **Userlist** -Abschnitt bezieht sich auf den Abschnitt **Verbinden** mit dem gleichen *Identifier* -Abschnittsparameter.

Dieser Abschnitt kann einen *Benutzerzugriffseintrag*enthalten, die durch den Zugriffsrechte für den angegebenen Benutzer und überschreibt die *standardmäßige* *Zugriffseintrag* im entsprechenden Abschnitt **Verbinden** .

## <a name="syntax"></a>Syntax

Ein Benutzerzugriffseintrag hat folgendes Format:

*UserName *** =* AccessRights ***

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
<td><p>Eines der folgenden Zugriffsrechte:
<br />
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

