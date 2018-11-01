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
# <a name="setmenuitem-macro-action"></a><span data-ttu-id="50536-102">SetzenMenüelement-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="50536-102">SetMenuItem Macro Action</span></span>


<span data-ttu-id="50536-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50536-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50536-104">Sie können die **SetzenMenüelement** -Aktion verwenden, um den Zustand des Menüelements (es kann aktiviert oder deaktiviert bzw. ausgewählt oder nicht ausgewählt sein) in benutzerdefinierten oder globalen Menüs auf der Registerkarte **Add-Ins** festzulegen.</span><span class="sxs-lookup"><span data-stu-id="50536-104">You can use the **SetMenuItem** action to set the state of menu items (enabled or disabled, selected or unselected) on custom or global menus on the **Add-Ins** tab.</span></span>


> [!NOTE]
> <P><span data-ttu-id="50536-p101">[!HINWEIS] Die <STRONG>SetzenMenüelement</STRONG> -Aktion kann nur in Kombination mit benutzerdefinierten und globalen Menüs verwendet werden, die mithilfe von Menümakros erstellt wurden. Die <STRONG>SetzenMenüelement</STRONG> -Aktion ist lediglich aus Gründen der Kompatibilität mit Vorgängerversionen in Microsoft Access enthalten. Die Aktion kann nicht in Kombination mit der Funktionalität Befehlsleiste verwendet werden. Sie können jedoch die Eigenschaften <STRONG>Aktiviert</STRONG> und <STRONG>Zustand</STRONG> in einem VBA-Modul (Visual Basic für Applikationen) verwenden, um Elemente in Kontextmenüs oder benutzerdefinierten bzw. globalen Menüs zu aktivieren oder deaktivieren und auszuwählen oder nicht auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="50536-p101">The <STRONG>SetMenuItem</STRONG> action works only with custom and global menus created by using menu macros. The <STRONG>SetMenuItem</STRONG> action is included in Microsoft Access only for compatibility with previous versions. It does not work with the command bar functionality. However, you can use the <STRONG>Enabled</STRONG> and <STRONG>State</STRONG> properties in a Visual Basic for Applications (VBA) module to disable or enable and select or unselect items on shortcut menus or custom or global menus.</span></span></P>



## <a name="setting"></a><span data-ttu-id="50536-109">Einstellung</span><span class="sxs-lookup"><span data-stu-id="50536-109">Setting</span></span>

<span data-ttu-id="50536-110">Die **SetzenMenüelement** -Aktion verwendet folgende Argumente.</span><span class="sxs-lookup"><span data-stu-id="50536-110">The **SetMenuItem** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50536-111">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="50536-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="50536-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50536-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50536-113"><strong>Menüindex</strong></span><span class="sxs-lookup"><span data-stu-id="50536-113"><strong>Menu Index</strong></span></span></p></td>
<td><p><span data-ttu-id="50536-114">Der Index des Menüs, das den Befehl enthält, für den Sie den Status festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="50536-114">The index of the menu that contains the command for which you want to set the state.</span></span> <span data-ttu-id="50536-115">Geben Sie einen Ganzzahlwert, beginnend bei 0, für den Index des gewünschten Menüs in der benutzerdefinierten oder globalen Menü aus.</span><span class="sxs-lookup"><span data-stu-id="50536-115">Enter an integer value, starting from 0, for the index of the desired menu in the custom or global menu.</span></span> <span data-ttu-id="50536-116">Geben Sie den Indexwert im Feld <strong>Menüindex</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators.</span><span class="sxs-lookup"><span data-stu-id="50536-116">Enter the index value in the <strong>Menu Index</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="50536-117">Der Index ist relativ zu der Position im Menümakro für das benutzerdefinierte oder globale Menü (die Position des dieses Menü <strong>HinzufügenMenü</strong> -Aktion im Menümakro, beginnend bei 0).</span><span class="sxs-lookup"><span data-stu-id="50536-117">The index is relative to the menu's position in the menu macro for the custom or global menu (the position of this menu's <strong>AddMenu</strong> action in the menu macro, counting from 0).</span></span> <span data-ttu-id="50536-118">Die Anzeige des Menüs möglicherweise etwas unterschiedlich sein, da Sie bedingte Ausdrücke im Menümakro verwenden können, um benutzerdefinierter Menüelemente anzeigen oder ausblenden.</span><span class="sxs-lookup"><span data-stu-id="50536-118">The menu's display may be somewhat different, because you can use conditional expressions in the menu macro to hide or display custom menu items.</span></span> <span data-ttu-id="50536-119">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="50536-119">This is a required argument.</span></span> <span data-ttu-id="50536-120">Wenn Sie ein Menü mit diesem Argument auswählen und die Argumente <strong>Befehlsindex</strong> und <strong>Unterbefehlsindex</strong> leer lassen, können Sie aktivieren oder deaktivieren den Namen des Menüs selbst.</span><span class="sxs-lookup"><span data-stu-id="50536-120">If you select a menu with this argument and leave the <strong>Command Index</strong> and <strong>Subcommand Index</strong> arguments blank, you can enable or disable the menu name itself.</span></span> <span data-ttu-id="50536-121">Sie können nicht jedoch markieren oder Markierung aufheben einer Menüname (Access ignoriert die <strong>Häkchen</strong> <strong>versehen</strong> und Einstellungen für das Argument <strong>Flag</strong> für die Menünamen von).</span><span class="sxs-lookup"><span data-stu-id="50536-121">You cannot, however, select or unselect a menu name (Access ignores the <strong>Check</strong> and <strong>Uncheck</strong> settings for the <strong>Flag</strong> argument for menu names).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50536-122"><strong>Befehlsindex</strong></span><span class="sxs-lookup"><span data-stu-id="50536-122"><strong>Command Index</strong></span></span></p></td>
<td><p><span data-ttu-id="50536-p103">Der Index des Befehls, für den Sie den Zustand festlegen möchten. Geben Sie einen Wert für eine ganze Zahl für den gewünschten Befehl in dem Menü ein, das über das Argument <strong>Menüindex</strong> ausgewählt wurde. Der Ausgangswert ist 0. Der Index verhält sich relativ zu der Position des Befehls in der Makrogruppe, die das ausgewählte Menü für das benutzerdefinierte oder globale Menü definiert (von 0 ausgehend gezählt die Position des Makros für diesen Befehl in der Makrogruppe). Die Anzeige des Menüs kann leicht abweichend sein, da bedingte Ausdrücke in der Makrogruppe des Menüs zum Anzeigen oder Ausblenden von benutzerdefinierten Menübefehlen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="50536-p103">The index of the command for which you want to set the state. Enter an integer value, starting from 0, for the index of the desired command in the menu selected by the <strong>Menu Index</strong> argument. The index is relative to the command's position in the macro group that defines the selected menu for the custom or global menu (the position of this command's macro in the macro group, counting from 0). The menu's display may be somewhat different, because you can use conditional expressions in the menu's macro group to hide or display custom menu commands.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50536-127"><strong>Unterbefehlsindex</strong></span><span class="sxs-lookup"><span data-stu-id="50536-127"><strong>Subcommand Index</strong></span></span></p></td>
<td><p><span data-ttu-id="50536-p104">Der Index des Unterbefehls, für den Sie den Zustand festlegen möchten. Dies gilt nur, wenn der gewünschte Befehl über ein Untermenü verfügt. Geben Sie einen Wert für eine ganze Zahl für den Index des gewünschten Unterbefehls in dem Untermenü ein, das über das Argument <strong>Befehlsindex</strong> ausgewählt wurde. Der Ausgangswert ist 0. Der Index verhält sich relativ zu der Position des Unterbefehls in der Makrogruppe, die das ausgewählte Untermenü für das benutzerdefinierte oder globale Menü definiert (von 0 ausgehend gezählt die Position des Makros für diesen Unterbefehl in der Makrogruppe).</span><span class="sxs-lookup"><span data-stu-id="50536-p104">The index of the subcommand for which you want to set the state. This applies only if the desired command has a submenu. Enter an integer value, starting from 0, for the index of the desired subcommand in the submenu selected by the <strong>Command Index</strong> argument. The index is relative to the subcommand's position in the macro group that defines the selected submenu for the custom or global menu (the position of this subcommand's macro in the macro group, counting from 0).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50536-132"><strong>Wert</strong></span><span class="sxs-lookup"><span data-stu-id="50536-132"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="50536-p105">Der Zustand, den Sie für den Befehl oder Unterbefehl festlegen möchten. Klicken Sie auf <strong>Deaktiviert</strong> (um den Befehl zu deaktivieren – dieser wird dann abgeblendet angezeigt), <strong>Aktiviert</strong> (um den Befehl zu aktivieren), <strong>Mit Häkchen</strong> (um den Befehl mit einem Häkchen zu versehen – dies bedeutet in der Regel, dass der Befehl ausgewählt oder eingeschaltet wurde) oder <strong>Ohne Häkchen</strong> (um das Häkchen zu entfernen). Die Standardeinstellung lautet <strong>Aktiviert</strong>.</span><span class="sxs-lookup"><span data-stu-id="50536-p105">The state you want to set the command or subcommand to. Click <strong>Gray</strong> (to disable the command — it appears dimmed), <strong>Ungray</strong> (to enable it), <strong>Check</strong> (to place a check by the command — typically indicating it has been selected or toggled), or <strong>Uncheck</strong> (to remove the check). The default is <strong>Ungray</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="50536-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50536-136">Remarks</span></span>

<span data-ttu-id="50536-p106">Die **SetzenMenüelement** -Aktion kann nur in Kombination mit einem benutzerdefinierten oder globalen Menü verwendet werden. Ist in dem aktiven Fenster kein entsprechendes Menü enthalten, wird durch die Ausführung eines Makros, in dem die **SetzenMenüelement** -Aktion enthalten ist, ein Laufzeitfehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="50536-p106">The **SetMenuItem** action works only on a custom or global menu. If the active window does not have a custom or global menu, running a macro containing the **SetMenuItem** action causes a run-time error.</span></span>

<span data-ttu-id="50536-139">Sie können diese Aktion verwenden, um den Zustand der Befehle und Unterbefehle in Menüs festzulegen. Die Aktion kann aber nicht für Unterbefehle von Unterbefehlen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50536-139">You can use this action to set the state of menu commands and subcommands, but not subcommands of subcommands.</span></span>

<span data-ttu-id="50536-140">Um die **SetzenMenüelement** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen, müssen Sie die **SetMenuItem** -Methode des **DoCmd** -Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="50536-140">To run the **SetMenuItem** action in a Visual Basic for Applications (VBA) module, use the **SetMenuItem** method of the **DoCmd** object.</span></span>

