---
title: AusführenMenübefehl-Makroaktion
TOCTitle: RunMenuCommand Macro Action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 372803779767ea6fdc12b4e10b5dde231ce101fc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875513"
---
# <a name="runmenucommand-macro-action"></a>AusführenMenübefehl-Makroaktion


**Betrifft**: Access 2013, Office 2013

Sie können die **AusführenMenübefehl** -Aktion verwenden, um einen integrierten Microsoft Access-Befehl auszuführen.

## <a name="setting"></a>Einstellung

Die **AusführenMenübefehl** -Aktion hat das folgende Aktionsargument.

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
<td><p><strong>Command</strong></p></td>
<td><p>Der Name des auszuführenden Befehls. In Access zeigt das Feld <strong>Befehl</strong> die verfügbaren integrierten Befehle in alphabetischer Reihenfolge an. Dies ist ein erforderliches Argument.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Sie können die **AusführenMenübefehl** -Aktion dazu verwenden, einen Access-Befehl aus einer benutzerdefinierten Menüleiste, einer globalen Menüleiste, einem benutzerdefinierten Kontextmenü oder einem globalen Kontextmenü auszuführen.

Um einen Befehl abhängig von bestimmten Bedingungen auszuführen, können Sie die **AusführenMenübefehl** -Aktion in einem Makro mit bedingten Ausdrücken verwenden.


> [!NOTE]
> <P>[!HINWEIS] Wenn Sie auf die Registerkarte <STRONG>Datei</STRONG> und dann auf <STRONG>Zuletzt verwendet</STRONG> klicken, werden die zuletzt verwendeten Datenbanken angezeigt. Anstatt auf <STRONG>Öffnen</STRONG> zu klicken, können Sie auf eine dieser Datenbanken klicken. Diese Datenbankelemente werden im Dropdown-Listenfeld für das Argument <STRONG>Befehl</STRONG> nicht angezeigt und sind durch Verwenden der <STRONG>AusführenMenübefehl</STRONG> -Aktion in einem Makro nicht verfügbar.</P>



Einige Befehle sind möglicherweise nicht mehr verfügbar, wenn Sie eine Access-Datenbank aus einer früheren Version von Access konvertieren. Ein Befehl ist möglicherweise umbenannt worden, in ein anderes Menü verschoben worden oder ist möglicherweise nicht mehr in Access verfügbar. Die in älteren Versionen verwendeten **AusführenMenübefehl** -Aktionen für solche Befehle können nicht in **AusführenMenübefehl** -Aktionen der neuen Version konvertiert werden. Access zeigt eine **AusführenMenübefehl** -Aktion mit einem leeren **Befehl** -Argument für solche Befehle an, wenn Sie das Makro öffnen. Sie müssen das Makro bearbeiten und ein gültiges Befehlsargument eingeben, oder Sie müssen die **AusführenMenübefehl** -Aktion löschen.

Verwenden Sie die **RunCommand** -Methode des **Application** -Objekts, um die **AusführenMenübefehl** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen. (Dies entspricht der **RunCommand** -Methode des **DoCmd** -Objekts.)

