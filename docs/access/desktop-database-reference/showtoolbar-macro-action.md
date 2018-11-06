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
ms.openlocfilehash: ed69a84f9b1774b7c33711a0bb8e80da54e656cc
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997930"
---
# <a name="showtoolbar-macro-action"></a>ShowToolbar-Makroaktion

**Betrifft**: Access 2013, Office 2013

Sie können die **EinblendenSymbolleiste** -Aktion zum Anzeigen oder Ausblenden von Befehlsgruppen auf der Registerkarte **Add-Ins** verwenden.

> [!NOTE]
> - [!HINWEIS] Die **EinblendenSymbolleiste** -Aktion wirkt sich nicht auf Kontextmenüs aus.
> - [!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **EinblendenSymbolleiste** -Aktion verwendet folgende Argumente.

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
<td><p>Der Name der Befehlgruppe auf der Registerkarte <strong>Add-Ins</strong> , die Sie anzeigen oder ausblenden möchten. Das Feld <strong>Symbolleistenname</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators zeigt die verfügbaren Gruppen, die durch diese Aktion beeinträchtigt werden können. Dies ist ein erforderliches Argument. Wenn Sie ein Makro ausführen, in dem die <strong>EinblendenSymbolleiste</strong>-Aktion in einer Bibliotheksdatenbank enthalten ist, sucht Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach der Gruppe mit diesem Namen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Show</strong></p></td>
<td><p>Gibt an, ob ein- oder Ausblenden der Gruppe und in welche Ansichten zum Anzeigen oder ausblenden. Der Standardwert ist <strong>Ja</strong> (der Gruppe jederzeit). Sie können <strong>Ja</strong> auswählen, um der Gruppe anzuzeigen überhaupt Zeiten <strong>, In dem entsprechenden</strong> zum Anzeigen der Gruppe nur, wenn das entsprechende Formular oder der Bericht aktiv ist, oder <strong>nicht</strong> um die Gruppe immer auszublenden.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Sie können diese Aktion in Makros verwenden, die bedingte Ausdrücke enthalten, um eine Gruppe in Abhängigkeit bestimmter Bedingungen anzuzeigen oder auszublenden.

Wenn Sie eine bestimmte Gruppe nur auf einem Formular oder Bericht einblenden möchten, können Sie die **BeiAktivierung** -Eigenschaft des Formulars oder Berichts für den Namen des Makros festlegen, in dem eine **EinblendenSymbolleiste** -Aktion enthalten ist, um die Gruppe einzublenden. Legen Sie anschließend die **BeiDeaktivierung** -Eigenschaft des Formulars oder Berichts für den Namen eines Makros fest, das eine **EinblendenSymbolleiste** -Aktion enthält, um die Gruppe auszublenden.

Die integrierten Symbolleisten können nicht über diese Aktion angezeigt oder ausgeblendet werden, wenn Sie die **AllowBuiltInToolbars** -Eigenschaft in einem VBA-Modul (Visual Basic für Applikationen) auf **Falsch** (0) festlegen, oder wenn Sie die Option **Integrierte Symbolleisten zulassen in VBA** auf **Falsch** festlegen, indem Sie die **SetOption** -Methode verwenden.

Um die **EinblendenSymbolleiste** -Aktion in einem VBA-Modul auszuführen, verwenden Sie die **ShowToolbar** -Methode des **DoCmd** -Objekts.

