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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280273"
---
# <a name="addmenu-macro-action"></a><span data-ttu-id="b6e59-102">AddMenu-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="b6e59-102">AddMenu macro action</span></span>


<span data-ttu-id="b6e59-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b6e59-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b6e59-104">Thema dieses Artikels ist die Makroaktion **HinzufügenMenü**.</span><span class="sxs-lookup"><span data-stu-id="b6e59-104">This article describes the basic operation of the **AddMenu** macro action.</span></span>

<span data-ttu-id="b6e59-105">Sie können die **HinzufügenMenü**-Aktion zum Erstellen folgender Elemente verwenden:</span><span class="sxs-lookup"><span data-stu-id="b6e59-105">You can use the **AddMenu** action to create:</span></span>

- <span data-ttu-id="b6e59-106">Benutzerdefinierte Menüs auf der Registerkarte **Add-Ins** für ein bestimmtes Formular oder einen bestimmten Bericht.</span><span class="sxs-lookup"><span data-stu-id="b6e59-106">Custom menus on the **Add-Ins** tab for a particular form or report.</span></span>

- <span data-ttu-id="b6e59-p101">Ein benutzerdefiniertes Kontextmenü für ein Formular, einen Bericht oder ein Formularsteuerelement. Das benutzerdefinierte Kontextmenü ersetzt das integrierte Kontextmenü für das Formular, den Bericht oder das Formularsteuerelement.</span><span class="sxs-lookup"><span data-stu-id="b6e59-p101">A custom shortcut menu for a form, report, or control. The custom shortcut menu replaces the built-in shortcut menu for the form, report, or control.</span></span>

- <span data-ttu-id="b6e59-p102">Ein globales Kontextmenü. Das globale Kontextmenü ersetzt das integrierte Kontextmenü für Felder in Tabellen- und Abfragedatenblättern, Formularen und Berichten. Dies gilt jedoch nicht für Fälle, in denen Sie ein benutzerdefiniertes Kontextmenü für ein Formular, einen Bericht oder ein Formularsteuerelement hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="b6e59-p102">A global shortcut menu. The global shortcut menu replaces the built-in shortcut menu for fields in table and query datasheets, forms, and reports, except where you've added a custom shortcut menu for a form, report, or control.</span></span>

## <a name="setting"></a><span data-ttu-id="b6e59-111">Einstellung</span><span class="sxs-lookup"><span data-stu-id="b6e59-111">Setting</span></span>

<span data-ttu-id="b6e59-112">Die **HinzufügenMenü**-Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="b6e59-112">The **AddMenu** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b6e59-113">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="b6e59-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b6e59-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6e59-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6e59-115"><strong>Menüname</strong></span><span class="sxs-lookup"><span data-stu-id="b6e59-115"><strong>Menu Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b6e59-116">Der Name &quot;des Menüs, beispielsweise Berichts Befehle&quot; oder &quot;-Tools.&quot;</span><span class="sxs-lookup"><span data-stu-id="b6e59-116">The name of the menu, for example, &quot;Report Commands&quot; or &quot;Tools&quot;.</span></span> <span data-ttu-id="b6e59-117">Um eine Zugriffstaste zu erstellen, damit Sie das Menü mithilfe der Tastatur auswählen können, geben Sie ein kaufmännisches und-Zeichen (<strong>&amp;</strong>) vor dem Buchstaben ein, der als Zugriffstaste verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6e59-117">To create an access key so that you can use the keyboard to choose the menu, type an ampersand (<strong>&amp;</strong>) before the letter you want to be the access key.</span></span> <span data-ttu-id="b6e59-118">Dieser Buchstabe wird im Menünamen auf der Registerkarte <strong>Add-Ins</strong> unterstrichen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b6e59-118">This letter will be underlined in the menu name on the <strong>Add-Ins</strong> tab.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6e59-119"><strong>Menümakroname</strong></span><span class="sxs-lookup"><span data-stu-id="b6e59-119"><strong>Menu Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b6e59-120">Der Name der Makrogruppe, die die Makros für die Menübefehle enthält.</span><span class="sxs-lookup"><span data-stu-id="b6e59-120">The name of the macro group that contains the macros for the menu's commands.</span></span> <span data-ttu-id="b6e59-121">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="b6e59-121">This is a required argument.</span></span></p>
<p><span data-ttu-id="b6e59-122"><strong>Hinweis</strong>: Wenn Sie ein Makro ausführen, das <strong></strong> die AddMenu-Aktion in einer Bibliotheksdatenbank enthält, sucht Microsoft Office Access 2007 nur in der aktuellen Datenbank nach der Makrogruppe mit diesem Namen.</span><span class="sxs-lookup"><span data-stu-id="b6e59-122"><strong>NOTE</strong>: If you run a macro containing the <strong>AddMenu</strong> action in a library database, Microsoft Office Access 2007 looks for the macro group with this name in the current database only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6e59-123"><strong>Statusleistentext</strong></span><span class="sxs-lookup"><span data-stu-id="b6e59-123"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="b6e59-124">Der Text, der in der Statusleiste angezeigt werden soll, wenn das Menü ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="b6e59-124">The text to display in the status bar when the menu is selected.</span></span> <span data-ttu-id="b6e59-125">Dieses Argument wird bei Kontextmenüs ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b6e59-125">This argument is ignored for shortcut menus.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b6e59-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6e59-126">Remarks</span></span>

<span data-ttu-id="b6e59-p106">Verwenden Sie die **AddMenu** -Methode des **DoCmd** -Objekts, um die **HinzufügenMenü** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen. Sie können auch die **MenuBar** - bzw. **ShortcutMenuBar** -Eigenschaft in VBA festlegen, um ein benutzerdefiniertes Menü auf der Registerkarte **Add-Ins** zu erstellen oder um ein benutzerdefiniertes Kontextmenü mit einem Formular, Bericht oder Formularsteuerelement zu verbinden. Sie können die **ShortcutMenuBar** -Eigenschaft des **Application** -Objekts festlegen, um ein globales Kontextmenü zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b6e59-p106">To run the **AddMenu** action in a Visual Basic for Applications (VBA) module, use the **AddMenu** method of the **DoCmd** object. You can also set the **MenuBar** or **ShortcutMenuBar** property in VBA to create a custom menu on the **Add-Ins** tab or to attach a custom shortcut menu to a form, report, or control. You can set the **ShortcutMenuBar** property of the **Application** object to create a global shortcut menu.</span></span>

