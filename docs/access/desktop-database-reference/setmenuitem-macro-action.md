---
title: SetMenuItem-Makroaktion
TOCTitle: SetMenuItem macro action
ms:assetid: 503b3635-e721-1b99-3249-626e5dccdb8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193803(v=office.15)
ms:contentKeyID: 48544789
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm16614
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: cda7c774e6af9f40d529fe809c49506a57c73c2b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568473"
---
# <a name="setmenuitem-macro-action"></a>SetMenuItem-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können die **SetzenMenüelement** -Aktion verwenden, um den Zustand des Menüelements (es kann aktiviert oder deaktiviert bzw. ausgewählt oder nicht ausgewählt sein) in benutzerdefinierten oder globalen Menüs auf der Registerkarte **Add-Ins** festzulegen.

> [!NOTE]
> [!HINWEIS] Die **SetzenMenüelement** -Aktion kann nur in Kombination mit benutzerdefinierten und globalen Menüs verwendet werden, die mithilfe von Menümakros erstellt wurden. Die **SetzenMenüelement** -Aktion ist lediglich aus Gründen der Kompatibilität mit Vorgängerversionen in Microsoft Access enthalten. Die Aktion kann nicht in Kombination mit der Funktionalität Befehlsleiste verwendet werden. Sie können jedoch die Eigenschaften **Aktiviert** und **Zustand** in einem VBA-Modul (Visual Basic für Applikationen) verwenden, um Elemente in Kontextmenüs oder benutzerdefinierten bzw. globalen Menüs zu aktivieren oder deaktivieren und auszuwählen oder nicht auszuwählen.

## <a name="setting"></a>Einstellung

Die **SetzenMenüelement**-Aktion verwendet folgende Argumente.

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
<td><p><strong>Menüindex</strong></p></td>
<td><p>Der Index des Menüs, das den Befehl enthält, für den Sie den Status festlegen möchten. Geben Sie einen ganzzahligen Wert ab 0 für den Index des gewünschten Menüs im benutzerdefinierten oder globalen Menü ein. Geben Sie den Indexwert in das <strong>Feld Menüindex</strong> im Abschnitt <strong>"Aktionsargumente"</strong> des Makro-Generator-Bereichs ein. Der Index ist relativ zur Menüposition im Menümakro für das benutzerdefinierte oder globale Menü (die Position der <strong>AddMenu-Aktion</strong> dieses Menüs im Menümakro, gezählt von 0). Die Anzeige des Menüs kann etwas anders sein, da Sie bedingte Ausdrücke im Menümakro verwenden können, um benutzerdefinierte Menüelemente auszublenden oder anzuzeigen. Dies ist ein erforderliches Argument. Wenn Sie ein Menü mit diesem Argument auswählen und die Argumente <strong>"Command Index"</strong> und <strong>"Subcommand Index"</strong> leer lassen, können Sie den Menünamen selbst aktivieren oder deaktivieren. Sie können jedoch keinen Menünamen auswählen oder die Auswahl aufheben (Access ignoriert die Einstellungen zum <strong>Aktivieren</strong> und <strong>Deaktivieren</strong> des <strong>Flag-Arguments</strong> für Menünamen).</p></td>
</tr>
<tr class="even">
<td><p><strong>Befehlsindex</strong></p></td>
<td><p>Der Index des Befehls, für den Sie den Zustand festlegen möchten. Geben Sie einen Wert für eine ganze Zahl für den gewünschten Befehl in dem Menü ein, das über das Argument <strong>Menüindex</strong> ausgewählt wurde. Der Ausgangswert ist 0. Der Index verhält sich relativ zu der Position des Befehls in der Makrogruppe, die das ausgewählte Menü für das benutzerdefinierte oder globale Menü definiert (von 0 ausgehend gezählt die Position des Makros für diesen Befehl in der Makrogruppe). Die Anzeige des Menüs kann leicht abweichend sein, da bedingte Ausdrücke in der Makrogruppe des Menüs zum Anzeigen oder Ausblenden von benutzerdefinierten Menübefehlen verwendet werden können.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Unterbefehlsindex</strong></p></td>
<td><p>Der Index des Unterbefehls, für den Sie den Zustand festlegen möchten. Dies gilt nur, wenn der gewünschte Befehl über ein Untermenü verfügt. Geben Sie einen Wert für eine ganze Zahl für den Index des gewünschten Unterbefehls in dem Untermenü ein, das über das Argument <strong>Befehlsindex</strong> ausgewählt wurde. Der Ausgangswert ist 0. Der Index verhält sich relativ zu der Position des Unterbefehls in der Makrogruppe, die das ausgewählte Untermenü für das benutzerdefinierte oder globale Menü definiert (von 0 ausgehend gezählt die Position des Makros für diesen Unterbefehl in der Makrogruppe).</p></td>
</tr>
<tr class="even">
<td><p><strong>Wert</strong></p></td>
<td><p>Der Zustand, den Sie für den Befehl oder Unterbefehl festlegen möchten. Klicken Sie auf <strong>Deaktiviert</strong> (um den Befehl zu deaktivieren – dieser wird dann abgeblendet angezeigt), <strong>Aktiviert</strong> (um den Befehl zu aktivieren), <strong>Mit Häkchen</strong> (um den Befehl mit einem Häkchen zu versehen – dies bedeutet in der Regel, dass der Befehl ausgewählt oder eingeschaltet wurde) oder <strong>Ohne Häkchen</strong> (um das Häkchen zu entfernen). Die Standardeinstellung lautet <strong>Aktiviert</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Die **SetzenMenüelement**-Aktion kann nur in Kombination mit einem benutzerdefinierten oder globalen Menü verwendet werden. Ist in dem aktiven Fenster kein entsprechendes Menü enthalten, wird durch die Ausführung eines Makros, in dem die **SetzenMenüelement**-Aktion enthalten ist, ein Laufzeitfehler verursacht.

Sie können diese Aktion verwenden, um den Zustand der Befehle und Unterbefehle in Menüs festzulegen. Die Aktion kann aber nicht für Unterbefehle von Unterbefehlen verwendet werden.

Um die **SetzenMenüelement**-Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen, müssen Sie die **SetMenuItem**-Methode des **DoCmd**-Objekts verwenden.

