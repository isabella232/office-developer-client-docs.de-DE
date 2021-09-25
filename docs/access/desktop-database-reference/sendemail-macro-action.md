---
title: SendEmail-Makroaktion
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 191942c63bce2111c22f2fbc871513a3c30c7a40
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585340"
---
# <a name="sendemail-macro-action"></a>SendEmail-Makroaktion

**Gilt für**: Access 2013, Office 2013

Die **SendEmail-Aktion** sendet eine E-Mail-Nachricht.

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
<td><p><strong>Bis</strong></p></td>
<td><p>Ja</p></td>
<td><p>Die Empfänger der Nachricht, deren Namen in die <strong>Zeile "An"</strong> der Nachricht eingefügt werden sollen. Trennen Sie die Empfängernamen, die Sie in diesem Argument (und in den <em>Argumenten Cc</em> und <em>Bcc)</em> angeben, durch ein Semikolon (;).</p></td>
</tr>
<tr class="even">
<td><p><strong>Cc</strong></p></td>
<td><p>Nein</p></td>
<td><p>Die Empfänger der Nachricht, deren Namen in die &quot; Cc-Zeile (Kopie) der Nachricht eingefügt werden &quot; sollen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Bcc</strong></p></td>
<td><p>Nein</p></td>
<td><p>Die Empfänger der Nachricht, deren Namen sie in die Bcc-Zeile &quot; (blind Carbon Copy) in der Nachricht einfügen &quot; möchten.</p></td>
</tr>
<tr class="even">
<td><p><strong>Betreff</strong></p></td>
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


## <a name="remarks"></a>HinwBemerkungeneise

Die **SendenEMail** -Aktion ist nur in den Makroereignissen **[Nach Löschvorgang](after-delete-macro-event.md)**, **[Nach Eingabe](after-insert-macro-event.md)** und **[Nach Aktualisierung](after-update-macro-event.md)** verfügbar.

Mit der **SendenEMail** -Aktion wird die Nachricht nicht zum Bearbeiten angezeigt.

