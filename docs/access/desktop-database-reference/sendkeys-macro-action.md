---
title: SendKeys-Makroaktion
TOCTitle: SendKeys macro action
ms:assetid: 3b06fcfc-ea64-c780-b5fc-6fc72853f524
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192656(v=office.15)
ms:contentKeyID: 48544275
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm183441
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: dda5d6fa69e60c84a76a62a091d429ca27ebfb1c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593600"
---
# <a name="sendkeys-macro-action"></a>SendKeys-Makroaktion

**Gilt für**: Access 2013, Office 2013

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Sicherheitshinweis" alt="Security note" /><strong>Sicherheitshinweis</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vermeiden Sie die <strong>SendKeys</strong>-Anweisung oder ein AutoKeys-Makro mit sensiblen oder vertraulichen Informationen. Ein böswilliger Benutzer kann die Tastatureingaben abfangen und die Sicherheit von Computer und Daten gefährden.</td>
</tr>
</tbody>
</table>

Sie können die **Tastaturbefehle** -Aktion zum direkten Senden von Tastaturbefehlen an Microsoft Access oder an eine aktive Windows-basierte Anwendung verwenden.

> [!NOTE]
> Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **Tastaturbefehle**-Aktion verwendet die folgenden Argumente.

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
<td><p><strong>Tastenanschläge</strong></p></td>
<td><p>Die Tastenanschläge, die Access oder die Anwendung verarbeiten soll. Geben Sie die Tastenanschläge im Feld <strong>"Tastaturbefehle"</strong> im Abschnitt <strong>"Aktionsargumente"</strong> des Makro-Generator-Bereichs ein. Sie können bis zu 255 Zeichen eingeben. Dies ist ein erforderliches Argument.</p></td>
</tr>
<tr class="even">
<td><p><strong>Wait</strong></p></td>
<td><p>Gibt an, ob das Makro angehalten werden soll, bis die Tastaturbefehle verarbeitet worden sind. Klicken Sie auf <strong>Ja</strong> (werden angehalten) oder <strong>Nein</strong> (werden nicht angehalten). Die Standardeinstellung ist <strong>Nein</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Access verarbeitet die Tastaturbefehle, die von der **Tastaturbefehle**-Aktion empfangen werden, als ob Sie diese direkt in einem Access-Fenster eingegeben hätten.

Um die Tastaturbefehle anzugeben, verwenden Sie dieselbe Syntax wie für die Anweisung **Tastaturbefehle**.

> [!NOTE]
> [!HINWEIS] Ein Fehler kann auftreten, wenn das Argument **Tastaturbefehle** falsche Syntax, falsch geschriebenen Text oder andere Werte enthält, die für das Fenster nicht geeignet sind, an die die Tastaturbefehle gesendet werden.

Wenn Sie das Makro nicht unterbrechen möchten, um manuell auf das Dialogfeld zu reagieren, können Sie diese Aktion verwenden, um Informationen in einem Dialogfeld einzugeben. In bestimmten, häufig verwendeten Dialogfeldern werden die Optionen durch einige Access-Aktionen, wie **Drucken** und **SuchenDatensatz**, ausgewählt. Um die Optionen auch in weniger häufiger verwendeten Dialogfeldern auszuwählen, können Sie die **Tastaturbefehle** -Aktion verwenden.

> [!NOTE]
> - Da das Dialogfeld das Makro unterbricht, müssen Sie die **Tastaturbefehle** -Aktion vor die Aktion stellen, die das Dialogfeld öffnet, und das Argument **Warten** auf **Nein** festlegen.
> - Der Zeitpunkt für die Tastaturbefehle, die Access oder eine andere Anwendung erreichen, kann ein Problem darstellen. Daher wird empfohlen, in den Fällen, in denen es eine andere Methode (wie die **SuchenDatensatz** -Aktion) zum Erzielen einer gewünschten Aufgabe gibt, diese statt der **Tastaturbefehle** -Aktion zur Auswahl der Optionen in einem Dialogfeld zu verwenden.

Wenn Sie mehr als 255 Zeichen an Access oder eine andere Windows-basierte Anwendung senden möchten, können Sie mehrere **Tastaturbefehle** -Aktionen in Folge in einem Makro verwenden.

Wenn die **Tastaturbefehle** -Aktion zum Senden von Tastaturbefehlen verwendet wird, wird das entsprechende Ereignis **KeyDown**, **KeyUp** und **KeyPress** ausgelöst. Wenn Nicht-ANSI-Tastaturbefehle gesendet werden (wie eine Funktionstaste), wird das **KeyPress** -Ereignis nicht ausgelöst.

Diese Aktion ist in einem Modul für Visual Basic für Applikationen (VBA) nicht verfügbar. Verwenden Sie stattdessen die Anweisung **Tastaturbefehle**.

