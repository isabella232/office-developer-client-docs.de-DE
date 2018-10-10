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
ms.openlocfilehash: 9d853c99fad322e17e8bbfd49cef27c14be33ffe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474543"
---
# <a name="runmenucommand-macro-action"></a><span data-ttu-id="8d4c1-102">AusführenMenübefehl-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="8d4c1-102">RunMenuCommand Macro Action</span></span>


<span data-ttu-id="8d4c1-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d4c1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8d4c1-104">Sie können die **AusführenMenübefehl** -Aktion verwenden, um einen integrierten Microsoft Access-Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8d4c1-104">You can use the **RunMenuCommand** action to run a built-in Microsoft Access command.</span></span>

## <a name="setting"></a><span data-ttu-id="8d4c1-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="8d4c1-105">Setting</span></span>

<span data-ttu-id="8d4c1-106">Die **AusführenMenübefehl** -Aktion hat das folgende Aktionsargument.</span><span class="sxs-lookup"><span data-stu-id="8d4c1-106">The **RunMenuCommand** action has the following action argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d4c1-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="8d4c1-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8d4c1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d4c1-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d4c1-109"><strong>Command</strong></span><span class="sxs-lookup"><span data-stu-id="8d4c1-109"><strong>Command</strong></span></span></p></td>
<td><p><span data-ttu-id="8d4c1-p101">Der Name des auszuführenden Befehls. In Access zeigt das Feld <strong>Befehl</strong> die verfügbaren integrierten Befehle in alphabetischer Reihenfolge an. Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="8d4c1-p101">The name of the command you want to run. The <strong>Command</strong> box shows the available built-in commands in Access, in alphabetical order. This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8d4c1-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d4c1-113">Remarks</span></span>

<span data-ttu-id="8d4c1-114">Sie können die **AusführenMenübefehl** -Aktion dazu verwenden, einen Access-Befehl aus einer benutzerdefinierten Menüleiste, einer globalen Menüleiste, einem benutzerdefinierten Kontextmenü oder einem globalen Kontextmenü auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8d4c1-114">You can use the **RunMenuCommand** action to run an Access command from a custom menu bar, global menu bar, custom shortcut menu, or global shortcut menu.</span></span>

<span data-ttu-id="8d4c1-115">Um einen Befehl abhängig von bestimmten Bedingungen auszuführen, können Sie die **AusführenMenübefehl** -Aktion in einem Makro mit bedingten Ausdrücken verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d4c1-115">You can use the **RunMenuCommand** action in a macro with conditional expressions to run a command depending on certain conditions.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8d4c1-p102">[!HINWEIS] Wenn Sie auf die Registerkarte <STRONG>Datei</STRONG> und dann auf <STRONG>Zuletzt verwendet</STRONG> klicken, werden die zuletzt verwendeten Datenbanken angezeigt. Anstatt auf <STRONG>Öffnen</STRONG> zu klicken, können Sie auf eine dieser Datenbanken klicken. Diese Datenbankelemente werden im Dropdown-Listenfeld für das Argument <STRONG>Befehl</STRONG> nicht angezeigt und sind durch Verwenden der <STRONG>AusführenMenübefehl</STRONG> -Aktion in einem Makro nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8d4c1-p102">Clicking the <STRONG>File</STRONG> tab and then clicking <STRONG>Recent</STRONG> shows the most recently used databases. You can click one of these databases instead of clicking <STRONG>Open</STRONG>. These database items don't appear in the drop-down list box for the <STRONG>Command</STRONG> argument, and aren't available by using the <STRONG>RunMenuCommand</STRONG> action in a macro.</span></span></P>



<span data-ttu-id="8d4c1-p103">Einige Befehle sind möglicherweise nicht mehr verfügbar, wenn Sie eine Access-Datenbank aus einer früheren Version von Access konvertieren. Ein Befehl ist möglicherweise umbenannt worden, in ein anderes Menü verschoben worden oder ist möglicherweise nicht mehr in Access verfügbar. Die in älteren Versionen verwendeten **AusführenMenübefehl** -Aktionen für solche Befehle können nicht in **AusführenMenübefehl** -Aktionen der neuen Version konvertiert werden. Access zeigt eine **AusführenMenübefehl** -Aktion mit einem leeren **Befehl** -Argument für solche Befehle an, wenn Sie das Makro öffnen. Sie müssen das Makro bearbeiten und ein gültiges Befehlsargument eingeben, oder Sie müssen die **AusführenMenübefehl** -Aktion löschen.</span><span class="sxs-lookup"><span data-stu-id="8d4c1-p103">When you convert an Access database from a previous version of Access, some commands may no longer be available. A command may have been renamed, moved to a different menu, or may no longer be available in Access. The **DoMenuItem** actions for such commands can't be converted to **RunMenuCommand** actions. When you open the macro, Access will display a **RunMenuCommand** action with a blank **Command** argument for such commands. You must edit the macro and enter a valid command argument, or delete the **RunMenuCommand** action.</span></span>

<span data-ttu-id="8d4c1-p104">Verwenden Sie die **RunCommand** -Methode des **Application** -Objekts, um die **AusführenMenübefehl** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen. (Dies entspricht der **RunCommand** -Methode des **DoCmd** -Objekts.)</span><span class="sxs-lookup"><span data-stu-id="8d4c1-p104">To run the **RunMenuCommand** action in a Visual Basic for Applications (VBA) module, use the **RunCommand** method of the **Application** object. (This is equivalent to the **RunCommand** method of the **DoCmd** object.)</span></span>

