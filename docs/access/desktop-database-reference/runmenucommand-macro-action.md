---
title: RunMenuCommand-Makroaktion
TOCTitle: RunMenuCommand macro action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c2b5a19b7a92fb68dfb774afeec5cd6ba456f38d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698162"
---
# <a name="runmenucommand-macro-action"></a><span data-ttu-id="18d58-102">RunMenuCommand-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="18d58-102">RunMenuCommand macro action</span></span>

<span data-ttu-id="18d58-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="18d58-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18d58-104">Sie können die **AusführenMenübefehl** -Aktion verwenden, um einen integrierten Microsoft Access-Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="18d58-104">You can use the **RunMenuCommand** action to run a built-in Microsoft Access command.</span></span>

## <a name="setting"></a><span data-ttu-id="18d58-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="18d58-105">Setting</span></span>

<span data-ttu-id="18d58-106">Die **AusführenMenübefehl** -Aktion hat das folgende Aktionsargument.</span><span class="sxs-lookup"><span data-stu-id="18d58-106">The **RunMenuCommand** action has the following action argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18d58-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="18d58-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="18d58-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18d58-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18d58-109"><strong>Command</strong></span><span class="sxs-lookup"><span data-stu-id="18d58-109"><strong>Command</strong></span></span></p></td>
<td><p><span data-ttu-id="18d58-p101">Der Name des auszuführenden Befehls. In Access zeigt das Feld <strong>Befehl</strong> die verfügbaren integrierten Befehle in alphabetischer Reihenfolge an. Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="18d58-p101">The name of the command you want to run. The <strong>Command</strong> box shows the available built-in commands in Access, in alphabetical order. This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="18d58-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="18d58-113">Remarks</span></span>

<span data-ttu-id="18d58-114">Sie können die **AusführenMenübefehl** -Aktion dazu verwenden, einen Access-Befehl aus einer benutzerdefinierten Menüleiste, einer globalen Menüleiste, einem benutzerdefinierten Kontextmenü oder einem globalen Kontextmenü auszuführen.</span><span class="sxs-lookup"><span data-stu-id="18d58-114">You can use the **RunMenuCommand** action to run an Access command from a custom menu bar, global menu bar, custom shortcut menu, or global shortcut menu.</span></span>

<span data-ttu-id="18d58-115">Um einen Befehl abhängig von bestimmten Bedingungen auszuführen, können Sie die **AusführenMenübefehl** -Aktion in einem Makro mit bedingten Ausdrücken verwenden.</span><span class="sxs-lookup"><span data-stu-id="18d58-115">You can use the **RunMenuCommand** action in a macro with conditional expressions to run a command depending on certain conditions.</span></span>

> [!NOTE]
> <span data-ttu-id="18d58-p102">[!HINWEIS] Wenn Sie auf die Registerkarte **Datei** und dann auf **Zuletzt verwendet** klicken, werden die zuletzt verwendeten Datenbanken angezeigt. Anstatt auf **Öffnen** zu klicken, können Sie auf eine dieser Datenbanken klicken. Diese Datenbankelemente werden im Dropdown-Listenfeld für das Argument **Befehl** nicht angezeigt und sind durch Verwenden der **AusführenMenübefehl** -Aktion in einem Makro nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="18d58-p102">Clicking the **File** tab and then clicking **Recent** shows the most recently used databases. You can click one of these databases instead of clicking **Open**. These database items don't appear in the drop-down list box for the **Command** argument, and aren't available by using the **RunMenuCommand** action in a macro.</span></span>

<span data-ttu-id="18d58-p103">Einige Befehle sind möglicherweise nicht mehr verfügbar, wenn Sie eine Access-Datenbank aus einer früheren Version von Access konvertieren. Ein Befehl ist möglicherweise umbenannt worden, in ein anderes Menü verschoben worden oder ist möglicherweise nicht mehr in Access verfügbar. Die in älteren Versionen verwendeten **AusführenMenübefehl** -Aktionen für solche Befehle können nicht in **AusführenMenübefehl** -Aktionen der neuen Version konvertiert werden. Access zeigt eine **AusführenMenübefehl** -Aktion mit einem leeren **Befehl** -Argument für solche Befehle an, wenn Sie das Makro öffnen. Sie müssen das Makro bearbeiten und ein gültiges Befehlsargument eingeben, oder Sie müssen die **AusführenMenübefehl** -Aktion löschen.</span><span class="sxs-lookup"><span data-stu-id="18d58-p103">When you convert an Access database from a previous version of Access, some commands may no longer be available. A command may have been renamed, moved to a different menu, or may no longer be available in Access. The **DoMenuItem** actions for such commands can't be converted to **RunMenuCommand** actions. When you open the macro, Access will display a **RunMenuCommand** action with a blank **Command** argument for such commands. You must edit the macro and enter a valid command argument, or delete the **RunMenuCommand** action.</span></span>

<span data-ttu-id="18d58-p104">Verwenden Sie die **RunCommand** -Methode des **Application** -Objekts, um die **AusführenMenübefehl** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen. (Dies entspricht der **RunCommand** -Methode des **DoCmd** -Objekts.)</span><span class="sxs-lookup"><span data-stu-id="18d58-p104">To run the **RunMenuCommand** action in a Visual Basic for Applications (VBA) module, use the **RunCommand** method of the **Application** object. (This is equivalent to the **RunCommand** method of the **DoCmd** object.)</span></span>

