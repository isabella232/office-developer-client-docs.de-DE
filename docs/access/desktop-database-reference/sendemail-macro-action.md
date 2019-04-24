---
title: SendEmail-Makroaktion
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c0fa220b3088cde46b0e82631c06520afd839c64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314651"
---
# <a name="sendemail-macro-action"></a>SendEmail-Makroaktion

**Gilt für**: Access 2013, Office 2013

Die **sendenemail** -Aktion sendet eine e-Mail-Nachricht.

> [!NOTE]
> Die **SendenEMail**-Aktion ist nur in Datenmakros verfügbar.

## <a name="setting"></a>Einstellung

Die **SendenEMail**-Aktion kann mit den folgenden Argumenten verwendet werden.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Erforderlich</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Ziel</strong></p></td>
<td><p>Ja</p></td>
<td><p>Die Empfänger der Nachricht, deren Namen Sie in der Nachricht an die <strong>an</strong> -Stelle setzen möchten. Trennen Sie die in diesem Argument angegebenen Empfängernamen (und in den Argumenten <em>CC</em> und <em>Bcc</em> ) mit einem Semikolon (;).</p></td>
</tr>
<tr class="even">
<td><p><strong>Cc</strong></p></td>
<td><p>Nein</p></td>
<td><p>Die Empfänger der Nachricht, deren Namen Sie der CC-Zeile (&quot;Carbon Copy&quot;) in der Nachricht hinzufügen möchten.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Bcc</strong></p></td>
<td><p>Nein</p></td>
<td><p>Die Empfänger der Nachricht, deren Namen Sie der Bcc-Zeile (&quot;Blind Carbon Copy&quot;) in der Nachricht hinzufügen möchten.</p></td>
</tr>
<tr class="even">
<td><p><strong>Subject</strong></p></td>
<td><p>Nein</p></td>
<td><p>Der Betreff der Nachricht. Dieser Text wird auf der Zeile <strong>Betreff</strong> der Nachricht angezeigt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Body</strong></p></td>
<td><p>Nein</p></td>
<td><p>Der Text, den Sie im Haupttext der E-Mail-Nachricht eingeben möchten. Wenn Sie dieses Argument leer lassen, wird kein zusätzlicher Text in der Nachricht eingeschlossen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Die **SendenEMail** -Aktion ist nur in den Makroereignissen **[Nach Löschvorgang](after-delete-macro-event.md)**, **[Nach Eingabe](after-insert-macro-event.md)** und **[Nach Aktualisierung](after-update-macro-event.md)** verfügbar.

Mit der **SendenEMail** -Aktion wird die Nachricht nicht zum Bearbeiten angezeigt.

