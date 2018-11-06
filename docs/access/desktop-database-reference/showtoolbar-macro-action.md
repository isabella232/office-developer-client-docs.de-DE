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
# <a name="showtoolbar-macro-action"></a><span data-ttu-id="fd18c-102">ShowToolbar-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="fd18c-102">ShowToolbar macro action</span></span>

<span data-ttu-id="fd18c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fd18c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fd18c-104">Sie können die **EinblendenSymbolleiste** -Aktion zum Anzeigen oder Ausblenden von Befehlsgruppen auf der Registerkarte **Add-Ins** verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd18c-104">You can use the **ShowToolbar** action to display or hide a group of commands on the **Add-Ins** tab.</span></span>

> [!NOTE]
> - <span data-ttu-id="fd18c-105">[!HINWEIS] Die **EinblendenSymbolleiste** -Aktion wirkt sich nicht auf Kontextmenüs aus.</span><span class="sxs-lookup"><span data-stu-id="fd18c-105">The **ShowToolbar** action does not affect shortcut menus.</span></span>
> - <span data-ttu-id="fd18c-106">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="fd18c-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="fd18c-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="fd18c-107">Setting</span></span>

<span data-ttu-id="fd18c-108">Die **EinblendenSymbolleiste** -Aktion verwendet folgende Argumente.</span><span class="sxs-lookup"><span data-stu-id="fd18c-108">The **ShowToolbar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fd18c-109">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="fd18c-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="fd18c-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd18c-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd18c-111"><strong>Symbolleistenname</strong></span><span class="sxs-lookup"><span data-stu-id="fd18c-111"><strong>Toolbar Name</strong></span></span></p></td>
<td><p><span data-ttu-id="fd18c-112">Der Name der Befehlgruppe auf der Registerkarte <strong>Add-Ins</strong> , die Sie anzeigen oder ausblenden möchten.</span><span class="sxs-lookup"><span data-stu-id="fd18c-112">The name of the command group on the <strong>Add-Ins</strong> tab you want to display or hide.</span></span> <span data-ttu-id="fd18c-113">Das Feld <strong>Symbolleistenname</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators zeigt die verfügbaren Gruppen, die durch diese Aktion beeinträchtigt werden können.</span><span class="sxs-lookup"><span data-stu-id="fd18c-113">The <strong>Toolbar Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane shows all the available groups that can be affected by this action.</span></span> <span data-ttu-id="fd18c-114">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="fd18c-114">This is a required argument.</span></span> <span data-ttu-id="fd18c-115">Wenn Sie ein Makro ausführen, in dem die <strong>EinblendenSymbolleiste</strong>-Aktion in einer Bibliotheksdatenbank enthalten ist, sucht Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach der Gruppe mit diesem Namen.</span><span class="sxs-lookup"><span data-stu-id="fd18c-115">If you run a macro containing the <strong>ShowToolbar</strong> action in a library database, Access first looks for the group with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd18c-116"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="fd18c-116"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="fd18c-117">Gibt an, ob ein- oder Ausblenden der Gruppe und in welche Ansichten zum Anzeigen oder ausblenden.</span><span class="sxs-lookup"><span data-stu-id="fd18c-117">Specifies whether to display or hide the group and in which views to display or hide it.</span></span> <span data-ttu-id="fd18c-118">Der Standardwert ist <strong>Ja</strong> (der Gruppe jederzeit).</span><span class="sxs-lookup"><span data-stu-id="fd18c-118">The default is <strong>Yes</strong> (show the group at all times).</span></span> <span data-ttu-id="fd18c-119">Sie können <strong>Ja</strong> auswählen, um der Gruppe anzuzeigen überhaupt Zeiten <strong>, In dem entsprechenden</strong> zum Anzeigen der Gruppe nur, wenn das entsprechende Formular oder der Bericht aktiv ist, oder <strong>nicht</strong> um die Gruppe immer auszublenden.</span><span class="sxs-lookup"><span data-stu-id="fd18c-119">You can select <strong>Yes</strong> to display the group at all times, <strong>Where Appropriate</strong> to display the group only when the appropriate form or report is active, or <strong>No</strong> to hide the group at all times.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fd18c-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fd18c-120">Remarks</span></span>

<span data-ttu-id="fd18c-121">Sie können diese Aktion in Makros verwenden, die bedingte Ausdrücke enthalten, um eine Gruppe in Abhängigkeit bestimmter Bedingungen anzuzeigen oder auszublenden.</span><span class="sxs-lookup"><span data-stu-id="fd18c-121">You can use this action in a macro with conditional expressions to display or hide a group depending on certain conditions.</span></span>

<span data-ttu-id="fd18c-p103">Wenn Sie eine bestimmte Gruppe nur auf einem Formular oder Bericht einblenden möchten, können Sie die **BeiAktivierung** -Eigenschaft des Formulars oder Berichts für den Namen des Makros festlegen, in dem eine **EinblendenSymbolleiste** -Aktion enthalten ist, um die Gruppe einzublenden. Legen Sie anschließend die **BeiDeaktivierung** -Eigenschaft des Formulars oder Berichts für den Namen eines Makros fest, das eine **EinblendenSymbolleiste** -Aktion enthält, um die Gruppe auszublenden.</span><span class="sxs-lookup"><span data-stu-id="fd18c-p103">If you want to show a particular group on just one form or report, you can set the **OnActivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to show the group. Then set the **OnDeactivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to hide the group.</span></span>

<span data-ttu-id="fd18c-124">Die integrierten Symbolleisten können nicht über diese Aktion angezeigt oder ausgeblendet werden, wenn Sie die **AllowBuiltInToolbars** -Eigenschaft in einem VBA-Modul (Visual Basic für Applikationen) auf **Falsch** (0) festlegen, oder wenn Sie die Option **Integrierte Symbolleisten zulassen in VBA** auf **Falsch** festlegen, indem Sie die **SetOption** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd18c-124">The built-in toolbars are not available to display or hide by using this action if you set the **AllowBuiltInToolbars** property to **False** (0) in a Visual Basic for Applications (VBA) module, or if you set the **Allow Built-in Toolbars** option to **False** in VBA by using the **SetOption** method.</span></span>

<span data-ttu-id="fd18c-125">Um die **EinblendenSymbolleiste** -Aktion in einem VBA-Modul auszuführen, verwenden Sie die **ShowToolbar** -Methode des **DoCmd** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="fd18c-125">To run the **ShowToolbar** action in a VBA module, use the **ShowToolbar** method of the **DoCmd** object.</span></span>

