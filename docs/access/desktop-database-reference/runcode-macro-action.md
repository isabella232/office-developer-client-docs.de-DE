---
title: RunCode-Makroaktion
TOCTitle: RunCode Macro Action
ms:assetid: cb0625be-4b5d-4927-9b0e-59a6e411b5bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834373(v=office.15)
ms:contentKeyID: 48547706
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98700
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c13f6fed20bebb40f4a8cacc3deedd7467ff55e4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472705"
---
# <a name="runcode-macro-action"></a><span data-ttu-id="05a83-102">RunCode-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="05a83-102">RunCode Macro Action</span></span>


<span data-ttu-id="05a83-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="05a83-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="05a83-104">Sie können mit der Aktion **AusführenCode** eine Visual Basic for Applications (VBA)-Funktionsprozedur aufrufen.</span><span class="sxs-lookup"><span data-stu-id="05a83-104">You can use the **RunCode** action to call a Visual Basic for Applications (VBA) Function procedure.</span></span>

## <a name="setting"></a><span data-ttu-id="05a83-105">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="05a83-105">Setting</span></span>

<span data-ttu-id="05a83-106">Die **AusführenCode** -Aktion hat das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="05a83-106">The **RunCode** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05a83-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="05a83-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="05a83-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05a83-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05a83-109"><strong>Funktionsname</strong></span><span class="sxs-lookup"><span data-stu-id="05a83-109"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="05a83-p101">Der Name der VBA-Funktionsprozedur, die aufgerufen werden soll. Geben Sie die gewünschten Funktionsargumente in Klammern an. Geben Sie den Funktionsnamenn im Feld <strong>Funktionsname</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs "Makro-Generator" ein. Dabei handelt es sich um ein Pflichtargument.  </span><span class="sxs-lookup"><span data-stu-id="05a83-p101">The name of the VBA Function procedure to call. Enclose any function arguments in parentheses. Enter the function name in the <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="05a83-p102">Klicken Sie in einer Access-Datenbank (.mdb oder .accdb) auf die Schaltfläche <STRONG>Erstellen</STRONG>, um mithilfe des Ausdrucks-Generators eine Funktion für dieses Argument auszuwählen. Klicken Sie dazu im Ausdrucks-Generator auf die gewünschte Funktion in der Liste.</span><span class="sxs-lookup"><span data-stu-id="05a83-p102">In an Access database (.mdb or .accdb), click the <STRONG>Build</STRONG> button to use the Expression Builder to select a function for this argument. Click the desired function in the list in the Expression Builder.</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="05a83-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="05a83-116">Remarks</span></span>

<span data-ttu-id="05a83-117">Die benutzerdefinierten Funktionen werden in Microsoft Access-Modulen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="05a83-117">The user-defined Function procedures are stored in Microsoft Access modules.</span></span>

<span data-ttu-id="05a83-118">Sie müssen Klammern angeben, auch wenn die Funktion, wie im folgenden Beispiel, über keine Argumente verfügt.</span><span class="sxs-lookup"><span data-stu-id="05a83-118">You must include parentheses, even if the Function procedure doesn't have any arguments, as in the following example:</span></span>

`TestFunction()`

<span data-ttu-id="05a83-119">Im Gegensatz zu benutzerdefinierten Funktionsnamen für Einstellungen der Ereignis-Eigenschaft verwendet, der Funktionsname im Argument **Funktionsname** nicht mit einem Gleichheitszeichen beginnen (**=**).</span><span class="sxs-lookup"><span data-stu-id="05a83-119">Unlike user-defined function names used for event property settings, the function name in the **Function Name** argument doesn't begin with an equal sign (**=**).</span></span>

<span data-ttu-id="05a83-120">Access ignoriert den Rückgabewert der Funktion.</span><span class="sxs-lookup"><span data-stu-id="05a83-120">Access ignores the return value of the function.</span></span>


> [!NOTE]
> <P><span data-ttu-id="05a83-121">[!HINWEIS] Sie können eine Funktionsprozedur nicht mit einem Makro aufrufen, wenn der Funktionsname dem Modulnamen entspricht.</span><span class="sxs-lookup"><span data-stu-id="05a83-121">You can't call a Function procedure from a macro if the function name is the same as the module name.</span></span></P>




> [!TIP]
> <P><span data-ttu-id="05a83-p103">[!TIPP] Um eine Sub- oder Ereignis-Prozedur in Visual Basic auszuführen, erstellen Sie eine Funktionsprozedur, die die entsprechende Sub- oder Ereignisprozedur aufruft. Führen Sie die Funktionsprozedur dann mit der Aktion <STRONG>AusführenCode</STRONG> aus.</span><span class="sxs-lookup"><span data-stu-id="05a83-p103">To run a Sub procedure or event procedure written in Visual Basic, create a Function procedure that calls the Sub procedure or event procedure. Then use the <STRONG>RunCode</STRONG> action to run the Function procedure.</span></span></P>



<span data-ttu-id="05a83-p104">Beim Aufrufen einer Funktion mit der Aktion **AusführenCode** sucht Access in den Standardmodulen der Datenbank nach einer Funktion mit dem Namen, der im Argument **Funktionsname** angegeben wurde. Wird die Aktion allerdings über einen Menübefehl oder ein Ereignis in einem Formular oder Bericht ausgeführt, sucht Access zuerst in den Klassenmodulen des Formulars bzw. Berichts und erst dann in den Standardmodulen. Die Klassenmodule im Bereich **Module** im Navigationsbereich werden nicht nach der Funktion durchsucht, deren Name im Argument **Funktionsname** angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="05a83-p104">If you use the **RunCode** action to call a function, Access looks for the function with the name specified by the **Function Name** argument in the standard modules for the database. However, when this action runs in response to clicking a menu command on a form or report or in response to an event on a form or report, Access first looks for the function in the form's or report's class module and then in the standard modules. Access doesn't search the class modules that appear in the **Modules** area of the Navigation Pane for the function specified by the **Function Name** argument.</span></span>

<span data-ttu-id="05a83-p105">Diese Aktion ist nicht in einem VBA-Modul verfügbar. Führen Sie die gewünschte Funktionsprozedur stattdessen direkt in VBA aus.</span><span class="sxs-lookup"><span data-stu-id="05a83-p105">This action isn't available in a VBA module. Instead, run the desired Function procedure directly in VBA.</span></span>

