---
title: AddMenu-Makroaktion
TOCTitle: AddMenu macro action
ms:assetid: 4eb2afa0-ed1f-41b1-d27f-b3ce7a73d2bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193760(v=office.15)
ms:contentKeyID: 48544762
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm37891
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 119e824cae71d54bb398aa68f476a667f14a6888
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699156"
---
# <a name="addmenu-macro-action"></a>AddMenu-Makroaktion


**Betrifft**: Access 2013, Office 2013

Thema dieses Artikels ist die Makroaktion **HinzufügenMenü**.

Sie können die **HinzufügenMenü** -Aktion zum Erstellen folgender Elemente verwenden:

- Benutzerdefinierte Menüs auf der Registerkarte **Add-Ins** für ein bestimmtes Formular oder einen bestimmten Bericht.

- Ein benutzerdefiniertes Kontextmenü für ein Formular, einen Bericht oder ein Formularsteuerelement. Das benutzerdefinierte Kontextmenü ersetzt das integrierte Kontextmenü für das Formular, den Bericht oder das Formularsteuerelement.

- Ein globales Kontextmenü. Das globale Kontextmenü ersetzt das integrierte Kontextmenü für Felder in Tabellen- und Abfragedatenblättern, Formularen und Berichten. Dies gilt jedoch nicht für Fälle, in denen Sie ein benutzerdefiniertes Kontextmenü für ein Formular, einen Bericht oder ein Formularsteuerelement hinzugefügt haben.

## <a name="setting"></a>Einstellung

Die **HinzufügenMenü** -Aktion hat die folgenden Argumente.

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
<td><p><strong>Menüname</strong></p></td>
<td><p>Der Name des auszuführenden Menüs, z. B. &quot;Berichtsbefehle&quot; oder &quot;Tools&quot;. Um eine Zugriffstaste zu erstellen, damit Sie die Tastatur verwenden können, klicken Sie im Menü auswählen, geben Sie ein kaufmännisches und-Zeichen (<strong>&amp;</strong>) vor dem Buchstaben der Zugriffstaste enthalten sein sollen. Dieser Buchstabe wird im Namen Menüs auf der Registerkarte ' <strong>Add-Ins</strong> ' unterstrichen dargestellt werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>Menümakroname</strong></p></td>
<td><p>Der Name der Makrogruppe, die die Makros für die Menübefehle enthält. Dies ist ein erforderliches Argument. 

</p>
<p><strong>Hinweis</strong>: Wenn Sie ein Makro, enthält die <strong>HinzufügenMenü</strong> -Aktion in einer Bibliotheksdatenbank ausführen, sucht Microsoft Office Access 2007 nach der Makrogruppe mit diesem Namen nur in der aktuellen Datenbank.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Statusleistentext</strong></p></td>
<td><p>Der Text, der in der Statusleiste angezeigt werden soll, wenn das Menü ausgewählt wird. Dieses Argument wird bei Kontextmenüs ignoriert.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Verwenden Sie die **AddMenu** -Methode des **DoCmd** -Objekts, um die **HinzufügenMenü** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen. Sie können auch die **MenuBar** - bzw. **ShortcutMenuBar** -Eigenschaft in VBA festlegen, um ein benutzerdefiniertes Menü auf der Registerkarte **Add-Ins** zu erstellen oder um ein benutzerdefiniertes Kontextmenü mit einem Formular, Bericht oder Formularsteuerelement zu verbinden. Sie können die **ShortcutMenuBar** -Eigenschaft des **Application** -Objekts festlegen, um ein globales Kontextmenü zu erstellen.

