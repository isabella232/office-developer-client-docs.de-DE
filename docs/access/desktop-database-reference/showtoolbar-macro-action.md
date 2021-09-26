---
title: ShowToolbar-Makroaktion
TOCTitle: ShowToolbar macro action
ms:assetid: 9e53009b-1e5e-1bee-3bcc-f82dc1b0dc48
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198288(v=office.15)
ms:contentKeyID: 48546649
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm27417
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 17a88c2b05c6bb66ab0d5e10c38bf17f302f2da4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611504"
---
# <a name="showtoolbar-macro-action"></a>ShowToolbar-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können die **EinblendenSymbolleiste** -Aktion zum Anzeigen oder Ausblenden von Befehlsgruppen auf der Registerkarte **Add-Ins** verwenden.

> [!NOTE]
> - [!HINWEIS] Die **EinblendenSymbolleiste** -Aktion wirkt sich nicht auf Kontextmenüs aus.
> - Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **EinblendenSymbolleiste**-Aktion verwendet folgende Argumente.

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
<td><p><strong>Symbolleistenname</strong></p></td>
<td><p>Der Name der Befehlsgruppe auf der Registerkarte <strong>"Add-Ins",</strong> die Sie anzeigen oder ausblenden möchten. Im Feld <strong>"Symbolleistenname"</strong> im Abschnitt <strong>"Aktionsargumente"</strong> des Makro-Generator-Bereichs werden alle verfügbaren Gruppen angezeigt, die von dieser Aktion betroffen sein können. Dies ist ein erforderliches Argument. Wenn Sie ein Makro ausführen, in dem die <strong>EinblendenSymbolleiste</strong>-Aktion in einer Bibliotheksdatenbank enthalten ist, sucht Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach der Gruppe mit diesem Namen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Show</strong></p></td>
<td><p>Gibt an, ob eine Gruppe angezeigt oder ausgeblendet wird und welche Ansichten zum Anzeigen oder Ausblenden verwendet werden. Der Standardwert ist <strong>Ja</strong> (die Gruppe jederzeit anzeigen). Sie können <strong>"Ja"</strong> auswählen, um die Gruppe jederzeit anzuzeigen. <strong>Gegebenenfalls</strong> wird die Gruppe nur angezeigt, wenn das entsprechende Formular oder der entsprechende Bericht aktiv ist, oder <strong>"Nein",</strong> um die Gruppe jederzeit auszublenden.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Sie können diese Aktion in Makros verwenden, die bedingte Ausdrücke enthalten, um eine Gruppe in Abhängigkeit bestimmter Bedingungen anzuzeigen oder auszublenden.

Wenn Sie eine bestimmte Gruppe nur auf einem Formular oder Bericht einblenden möchten, können Sie die **BeiAktivierung** -Eigenschaft des Formulars oder Berichts für den Namen des Makros festlegen, in dem eine **EinblendenSymbolleiste** -Aktion enthalten ist, um die Gruppe einzublenden. Legen Sie anschließend die **BeiDeaktivierung** -Eigenschaft des Formulars oder Berichts für den Namen eines Makros fest, das eine **EinblendenSymbolleiste** -Aktion enthält, um die Gruppe auszublenden.

Die integrierten Symbolleisten können nicht über diese Aktion angezeigt oder ausgeblendet werden, wenn Sie die **AllowBuiltInToolbars** -Eigenschaft in einem VBA-Modul (Visual Basic für Applikationen) auf **Falsch** (0) festlegen, oder wenn Sie die Option **Integrierte Symbolleisten zulassen in VBA** auf **Falsch** festlegen, indem Sie die **SetOption** -Methode verwenden.

Um die **EinblendenSymbolleiste** -Aktion in einem VBA-Modul auszuführen, verwenden Sie die **ShowToolbar** -Methode des **DoCmd** -Objekts.

