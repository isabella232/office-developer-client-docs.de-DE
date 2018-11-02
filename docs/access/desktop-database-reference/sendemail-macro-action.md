---
title: SendEmail-Makroaktion
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aa783dcc7ad02cc36b14ef9ef97436cb1ad88e4a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924687"
---
# <a name="sendemail-macro-action"></a>SendEmail-Makroaktion


**Betrifft**: Access 2013, Office 2013

Mit der **SendenEMail** -Aktion senden Sie eine E-Mail-Nachricht.


> [!NOTE]
> <P>[!HINWEIS] Die <STRONG>SendenEMail</STRONG> -Aktion ist nur in Datenmakros verfügbar.</P>



## <a name="setting"></a>Einstellung

Die **SendenEMail** -Aktion kann mit den folgenden Argumenten verwendet werden.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Eingabe erforderlich</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>An</strong></p></td>
<td><p>Ja</p></td>
<td><p>Die Empfänger der Nachricht, deren Namen Sie in der Zeile <strong>an</strong> , in der Nachricht aufnehmen möchten. Trennen Sie die Namen die Empfänger, die Sie in diesem Argument (und in den Argumenten <em>Cc</em> und <em>Bcc</em> ) durch ein Semikolon (;) angeben.</p></td>
</tr>
<tr class="even">
<td><p><strong>Cc</strong></p></td>
<td><p>Nein</p></td>
<td><p>Die Empfänger der Nachricht, deren Namen Sie in der Cc aufnehmen möchten (&quot;Carbon Copy, Blindkopie&quot;) Zeile der Nachricht.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Bcc</strong></p></td>
<td><p>Nein</p></td>
<td><p>Die Empfänger der Nachricht, deren Namen Sie in der Bcc aufnehmen möchten (&quot;blind Carbon Copy, Blindkopie&quot;) Zeile der Nachricht.</p></td>
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


## <a name="remarks"></a>Hinweise

Die **SendenEMail** -Aktion ist nur in den Makroereignissen **[Nach Löschvorgang](after-delete-macro-event.md)**, **[Nach Eingabe](after-insert-macro-event.md)** und **[Nach Aktualisierung](after-update-macro-event.md)** verfügbar.

Mit der **SendenEMail** -Aktion wird die Nachricht nicht zum Bearbeiten angezeigt.

