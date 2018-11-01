---
title: Tastaturbefehle-Makroaktion
TOCTitle: SendKeys Macro Action
ms:assetid: 3b06fcfc-ea64-c780-b5fc-6fc72853f524
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192656(v=office.15)
ms:contentKeyID: 48544275
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm183441
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3f8ddc6c19f675db7cc04cb46a24e0f42ac991df
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881356"
---
# <a name="sendkeys-macro-action"></a>Tastaturbefehle-Makroaktion


**Betrifft**: Access 2013, Office 2013

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Sicherheitshinweis" alt="Security note" /><strong>Sicherheitshinweis</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>
      Vermeiden Sie bei sensiblen oder vertraulichen Informationen die Verwendung der <strong>SendKeys</strong>-Anweisung oder eines AutoKeys-Makros. Ein bösartiger Benutzer könnte die Tastenfolgen abfangen und die Sicherheit Ihres Computers und Ihrer Daten gefährden.
</td>
</tr>
</tbody>
</table>


Sie können die **Tastaturbefehle** -Aktion zum direkten Senden von Tastaturbefehlen an Microsoft Access oder an eine aktive Windows-basierte Anwendung verwenden.


> [!NOTE]
> <P>[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</P>



## <a name="setting"></a>Einstellung

Die **Tastaturbefehle** -Aktion verwendet die folgenden Argumente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktionsargument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Tastaturbefehle</strong></p></td>
<td><p>Die Tastaturbefehle, die Access oder die Anwendung verarbeiten soll. Geben Sie die Tastaturbefehle im Feld Tastaturbefehle im Abschnitt Aktionsargumente im Bereichs Makro-Generator ein. Sie können bis zu 255 Zeichen eingeben. Dies ist ein erforderliches Argument.</p></td>
</tr>
<tr class="even">
<td><p><strong>Wait</strong></p></td>
<td><p>Gibt an, ob das Makro angehalten werden soll, bis die Tastaturbefehle verarbeitet worden sind. Klicken Sie auf <strong>Ja</strong> (werden angehalten) oder <strong>Nein</strong> (werden nicht angehalten). Die Standardeinstellung ist <strong>Nein</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Access verarbeitet die Tastaturbefehle, die von der **Tastaturbefehle** -Aktion empfangen werden, als ob Sie diese direkt in einem Access-Fenster eingegeben hätten.

Um die Tastaturbefehle anzugeben, verwenden Sie dieselbe Syntax wie für die Anweisung **Tastaturbefehle**.


> [!NOTE]
> <P>[!HINWEIS] Ein Fehler kann auftreten, wenn das Argument <STRONG>Tastaturbefehle</STRONG> falsche Syntax, falsch geschriebenen Text oder andere Werte enthält, die für das Fenster nicht geeignet sind, an die die Tastaturbefehle gesendet werden.</P>



Wenn Sie das Makro nicht unterbrechen möchten, um manuell auf das Dialogfeld zu reagieren, können Sie diese Aktion verwenden, um Informationen in einem Dialogfeld einzugeben. In bestimmten, häufig verwendeten Dialogfeldern werden die Optionen durch einige Access-Aktionen, wie **Drucken** und **SuchenDatensatz**, ausgewählt. Um die Optionen auch in weniger häufiger verwendeten Dialogfeldern auszuwählen, können Sie die **Tastaturbefehle** -Aktion verwenden.


> [!NOTE]
> <UL>
> <LI>
> <P>Da das Dialogfeld das Makro unterbricht, müssen Sie die <STRONG>Tastaturbefehle</STRONG> -Aktion vor die Aktion stellen, die das Dialogfeld öffnet, und das Argument <STRONG>Warten</STRONG> auf <STRONG>Nein</STRONG> festlegen.</P>
> <LI>
> <P>Der Zeitpunkt für die Tastaturbefehle, die Access oder eine andere Anwendung erreichen, kann ein Problem darstellen. Daher wird empfohlen, in den Fällen, in denen es eine andere Methode (wie die <STRONG>SuchenDatensatz</STRONG> -Aktion) zum Erzielen einer gewünschten Aufgabe gibt, diese statt der <STRONG>Tastaturbefehle</STRONG> -Aktion zur Auswahl der Optionen in einem Dialogfeld zu verwenden.</P></LI></UL>



Wenn Sie mehr als 255 Zeichen an Access oder eine andere Windows-basierte Anwendung senden möchten, können Sie mehrere **Tastaturbefehle** -Aktionen in Folge in einem Makro verwenden.

Wenn die **Tastaturbefehle** -Aktion zum Senden von Tastaturbefehlen verwendet wird, wird das entsprechende Ereignis **KeyDown**, **KeyUp** und **KeyPress** ausgelöst. Wenn Nicht-ANSI-Tastaturbefehle gesendet werden (wie eine Funktionstaste), wird das **KeyPress** -Ereignis nicht ausgelöst.

Diese Aktion ist in einem Modul für Visual Basic für Applikationen (VBA) nicht verfügbar. Verwenden Sie stattdessen die Anweisung **Tastaturbefehle**.

