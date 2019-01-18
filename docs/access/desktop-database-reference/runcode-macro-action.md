---
title: RunCode-Makroaktion
TOCTitle: RunCode macro action
ms:assetid: cb0625be-4b5d-4927-9b0e-59a6e411b5bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834373(v=office.15)
ms:contentKeyID: 48547706
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98700
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 646c1393cc798c1f827e6ceaebf46bfe7c87bcbd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722382"
---
# <a name="runcode-macro-action"></a><span data-ttu-id="fcc41-102">RunCode-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="fcc41-102">RunCode macro action</span></span>

<span data-ttu-id="fcc41-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fcc41-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fcc41-104">Sie können mit der Aktion **AusführenCode** eine Visual Basic for Applications (VBA)-Funktionsprozedur aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fcc41-104">You can use the **RunCode** action to call a Visual Basic for Applications (VBA) Function procedure.</span></span>

## <a name="setting"></a><span data-ttu-id="fcc41-105">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="fcc41-105">Setting</span></span>

<span data-ttu-id="fcc41-106">Die **AusführenCode** -Aktion hat das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="fcc41-106">The **RunCode** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fcc41-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="fcc41-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="fcc41-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fcc41-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcc41-109"><strong>Funktionsname</strong></span><span class="sxs-lookup"><span data-stu-id="fcc41-109"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="fcc41-p101">Der Name der VBA-Funktionsprozedur, die aufgerufen werden soll. Geben Sie die gewünschten Funktionsargumente in Klammern an. Geben Sie den Funktionsnamenn im Feld <strong>Funktionsname</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs "Makro-Generator" ein. Dabei handelt es sich um ein Pflichtargument.  </span><span class="sxs-lookup"><span data-stu-id="fcc41-p101">The name of the VBA Function procedure to call. Enclose any function arguments in parentheses. Enter the function name in the <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p><p><span data-ttu-id="fcc41-114"><strong>Hinweis</strong>: In einer Access-Datenbank (MDB oder ACCDB), klicken Sie auf die <strong>Generator</strong> -Schaltfläche des Ausdrucks-Generators verwenden, um eine Funktion für dieses Argument auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="fcc41-114"><strong>NOTE</strong>: In an Access database (.mdb or .accdb), click the <strong>Build</strong> button to use the Expression Builder to select a function for this argument.</span></span> <span data-ttu-id="fcc41-115">Klicken Sie auf die gewünschte Funktion in der Liste im Ausdrucks-Generator.</span><span class="sxs-lookup"><span data-stu-id="fcc41-115">Click the desired function in the list in the Expression Builder.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fcc41-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fcc41-116">Remarks</span></span>

<span data-ttu-id="fcc41-117">Die benutzerdefinierten Funktionen werden in Microsoft Access-Modulen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fcc41-117">The user-defined Function procedures are stored in Microsoft Access modules.</span></span>

<span data-ttu-id="fcc41-118">Sie müssen Klammern angeben, auch wenn die Funktion, wie im folgenden Beispiel, über keine Argumente verfügt.</span><span class="sxs-lookup"><span data-stu-id="fcc41-118">You must include parentheses, even if the Function procedure doesn't have any arguments, as in the following example:</span></span>

`TestFunction()`

<span data-ttu-id="fcc41-119">Im Gegensatz zu benutzerdefinierten Funktionsnamen für Einstellungen der Ereignis-Eigenschaft verwendet, der Funktionsname im Argument **Funktionsname** nicht mit einem Gleichheitszeichen beginnen (**=**).</span><span class="sxs-lookup"><span data-stu-id="fcc41-119">Unlike user-defined function names used for event property settings, the function name in the **Function Name** argument doesn't begin with an equal sign (**=**).</span></span>

<span data-ttu-id="fcc41-120">Access ignoriert den Rückgabewert der Funktion.</span><span class="sxs-lookup"><span data-stu-id="fcc41-120">Access ignores the return value of the function.</span></span>

> [!NOTE]
> <span data-ttu-id="fcc41-121">[!HINWEIS] Sie können eine Funktionsprozedur nicht mit einem Makro aufrufen, wenn der Funktionsname dem Modulnamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="fcc41-121">You can't call a Function procedure from a macro if the function name is the same as the module name.</span></span>

> [!TIP]
> <span data-ttu-id="fcc41-p103">[!TIPP] Um eine Sub- oder Ereignis-Prozedur in Visual Basic auszuführen, erstellen Sie eine Funktionsprozedur, die die entsprechende Sub- oder Ereignisprozedur aufruft. Führen Sie die Funktionsprozedur dann mit der Aktion **AusführenCode** aus.</span><span class="sxs-lookup"><span data-stu-id="fcc41-p103">To run a Sub procedure or event procedure written in Visual Basic, create a Function procedure that calls the Sub procedure or event procedure. Then use the **RunCode** action to run the Function procedure.</span></span>

<span data-ttu-id="fcc41-p104">Beim Aufrufen einer Funktion mit der Aktion **AusführenCode** sucht Access in den Standardmodulen der Datenbank nach einer Funktion mit dem Namen, der im Argument **Funktionsname** angegeben wurde. Wird die Aktion allerdings über einen Menübefehl oder ein Ereignis in einem Formular oder Bericht ausgeführt, sucht Access zuerst in den Klassenmodulen des Formulars bzw. Berichts und erst dann in den Standardmodulen. Die Klassenmodule im Bereich **Module** im Navigationsbereich werden nicht nach der Funktion durchsucht, deren Name im Argument **Funktionsname** angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="fcc41-p104">If you use the **RunCode** action to call a function, Access looks for the function with the name specified by the **Function Name** argument in the standard modules for the database. However, when this action runs in response to clicking a menu command on a form or report or in response to an event on a form or report, Access first looks for the function in the form's or report's class module and then in the standard modules. Access doesn't search the class modules that appear in the **Modules** area of the Navigation Pane for the function specified by the **Function Name** argument.</span></span>

<span data-ttu-id="fcc41-p105">Diese Aktion ist nicht in einem VBA-Modul verfügbar. Führen Sie die gewünschte Funktionsprozedur stattdessen direkt in VBA aus.</span><span class="sxs-lookup"><span data-stu-id="fcc41-p105">This action isn't available in a VBA module. Instead, run the desired Function procedure directly in VBA.</span></span>

