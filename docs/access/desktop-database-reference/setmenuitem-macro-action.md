---
title: SetzenMenüelement-Makroaktion
TOCTitle: SetMenuItem Macro Action
ms:assetid: 503b3635-e721-1b99-3249-626e5dccdb8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193803(v=office.15)
ms:contentKeyID: 48544789
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm16614
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d7a7de3d627dacfa0ca014a80ea037d0728220d1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873565"
---
# <a name="setmenuitem-macro-action"></a>SetzenMenüelement-Makroaktion


**Betrifft**: Access 2013, Office 2013

Sie können die **SetzenMenüelement** -Aktion verwenden, um den Zustand des Menüelements (es kann aktiviert oder deaktiviert bzw. ausgewählt oder nicht ausgewählt sein) in benutzerdefinierten oder globalen Menüs auf der Registerkarte **Add-Ins** festzulegen.


> [!NOTE]
> <P>[!HINWEIS] Die <STRONG>SetzenMenüelement</STRONG> -Aktion kann nur in Kombination mit benutzerdefinierten und globalen Menüs verwendet werden, die mithilfe von Menümakros erstellt wurden. Die <STRONG>SetzenMenüelement</STRONG> -Aktion ist lediglich aus Gründen der Kompatibilität mit Vorgängerversionen in Microsoft Access enthalten. Die Aktion kann nicht in Kombination mit der Funktionalität Befehlsleiste verwendet werden. Sie können jedoch die Eigenschaften <STRONG>Aktiviert</STRONG> und <STRONG>Zustand</STRONG> in einem VBA-Modul (Visual Basic für Applikationen) verwenden, um Elemente in Kontextmenüs oder benutzerdefinierten bzw. globalen Menüs zu aktivieren oder deaktivieren und auszuwählen oder nicht auszuwählen.</P>



## <a name="setting"></a>Einstellung

Die **SetzenMenüelement** -Aktion verwendet folgende Argumente.

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
<td><p>Der Index des Menüs, das den Befehl enthält, für den Sie den Status festlegen möchten. Geben Sie einen Ganzzahlwert, beginnend bei 0, für den Index des gewünschten Menüs in der benutzerdefinierten oder globalen Menü aus. Geben Sie den Indexwert im Feld <strong>Menüindex</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators. Der Index ist relativ zu der Position im Menümakro für das benutzerdefinierte oder globale Menü (die Position des dieses Menü <strong>HinzufügenMenü</strong> -Aktion im Menümakro, beginnend bei 0). Die Anzeige des Menüs möglicherweise etwas unterschiedlich sein, da Sie bedingte Ausdrücke im Menümakro verwenden können, um benutzerdefinierter Menüelemente anzeigen oder ausblenden. Dies ist ein erforderliches Argument. Wenn Sie ein Menü mit diesem Argument auswählen und die Argumente <strong>Befehlsindex</strong> und <strong>Unterbefehlsindex</strong> leer lassen, können Sie aktivieren oder deaktivieren den Namen des Menüs selbst. Sie können nicht jedoch markieren oder Markierung aufheben einer Menüname (Access ignoriert die <strong>Häkchen</strong> <strong>versehen</strong> und Einstellungen für das Argument <strong>Flag</strong> für die Menünamen von).</p></td>
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


## <a name="remarks"></a>Hinweise

Die **SetzenMenüelement** -Aktion kann nur in Kombination mit einem benutzerdefinierten oder globalen Menü verwendet werden. Ist in dem aktiven Fenster kein entsprechendes Menü enthalten, wird durch die Ausführung eines Makros, in dem die **SetzenMenüelement** -Aktion enthalten ist, ein Laufzeitfehler verursacht.

Sie können diese Aktion verwenden, um den Zustand der Befehle und Unterbefehle in Menüs festzulegen. Die Aktion kann aber nicht für Unterbefehle von Unterbefehlen verwendet werden.

Um die **SetzenMenüelement** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen, müssen Sie die **SetMenuItem** -Methode des **DoCmd** -Objekts verwenden.

