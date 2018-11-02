---
title: RunMacro-Makroaktion
TOCTitle: RunMacro macro action
ms:assetid: 25966f20-8160-0821-b88a-ed08b7786fdc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191868(v=office.15)
ms:contentKeyID: 48543787
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm43195
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7aace8618e9ca5cdd540c15d04869dbce8c3a891
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926115"
---
# <a name="runmacro-macro-action"></a><span data-ttu-id="9f2d4-102">RunMacro-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="9f2d4-102">RunMacro macro action</span></span>


<span data-ttu-id="9f2d4-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f2d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9f2d4-p101">Zum Ausführen eines Makros können Sie die **AusführenMakro** -Aktion verwenden. Das Makro kann sich in einer Makrogruppe befinden.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-p101">You can use the **RunMacro** action to run a macro. The macro can be in a macro group.</span></span>

<span data-ttu-id="9f2d4-106">Sie können diese Aktion für Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="9f2d4-106">You can use this action:</span></span>

  - <span data-ttu-id="9f2d4-107">Zum Ausführen eines Makros innerhalb eines anderen Makros.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-107">To run a macro from within another macro.</span></span>

  - <span data-ttu-id="9f2d4-108">Zum Ausführen eines Makros basierend auf einer bestimmten Bedingung.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-108">To run a macro based on a certain condition.</span></span>

  - <span data-ttu-id="9f2d4-109">Zum Anfügen eines Makros an einen benutzerdefinierten Menübefehl.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-109">To attach a macro to a custom menu command.</span></span>

## <a name="setting"></a><span data-ttu-id="9f2d4-110">Einstellung</span><span class="sxs-lookup"><span data-stu-id="9f2d4-110">Setting</span></span>

<span data-ttu-id="9f2d4-111">Die **AusführenMakro** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-111">The **RunMacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9f2d4-112">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="9f2d4-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="9f2d4-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f2d4-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f2d4-114"><strong>Makroname</strong></span><span class="sxs-lookup"><span data-stu-id="9f2d4-114"><strong>Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="9f2d4-115">Der Name des auzuführenden Makros.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-115">The name of the macro to run.</span></span> <span data-ttu-id="9f2d4-116">Das Feld <strong>Makroname</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators zeigt alle Makros (und Makrogruppen) in der aktuellen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-116">The <strong>Macro Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all macros (and macro groups) in the current database.</span></span> <span data-ttu-id="9f2d4-117">Wenn das Makro in einer Makrogruppe befindet, wird sie als <em>Makrogruppenname</em>unter dem Makrogruppennamen in der Liste aufgeführt. <em>Makroname</em>.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-117">If the macro is in a macro group, it's listed under the macro group name in the list as <em>macrogroupname</em>.<em>macroname</em>.</span></span> <span data-ttu-id="9f2d4-118">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-118">This is a required argument.</span></span> <span data-ttu-id="9f2d4-119">Wenn Sie ein Makro ausführen, das die <strong>AusführenMakro</strong>-Aktion in einer Bibliotheksdatenbank enthält, sucht Microsoft Access zunächst in der Bibliotheksdatenbank nach dem Makro mit diesem Namen und dann in der aktuellen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-119">If you run a macro containing the <strong>RunMacro</strong> action in a library database, Microsoft Access looks for the macro with this name in the library database and doesn't look for it in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f2d4-120"><strong>Wiederholungen</strong></span><span class="sxs-lookup"><span data-stu-id="9f2d4-120"><strong>Repeat Count</strong></span></span></p></td>
<td><p><span data-ttu-id="9f2d4-p103">Gibt an, wie oft das Makro maximal ausgeführt wird. Wenn Sie dieses Argument leer lassen (und das Argument <strong>Wiederholungen</strong> auch leer ist), wird das Makro einmal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-p103">The maximum number of times the macro will run. If you leave this argument blank (and the <strong>Repeat Expression</strong> argument is also blank), the macro runs once.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f2d4-123"><strong>Wiederholbedingung</strong></span><span class="sxs-lookup"><span data-stu-id="9f2d4-123"><strong>Repeat Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="9f2d4-p104">Ein Ausdruck, der mit <strong>Wahr</strong> (-1) oder <strong>Falsch</strong> (0) ausgewertet wird. Das Makro beendet die Ausführung des Makros, wenn der Ausdruck als <strong>Falsch</strong> ausgewertet wird. Der Ausdruck wird bei jeder Makroausführung ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-p104">An expression that evaluates to <strong>True</strong> (–1) or <strong>False</strong> (0). The macro stops running if the expression evaluates to <strong>False</strong>. The expression is evaluated each time the macro runs.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9f2d4-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9f2d4-127">Remarks</span></span>

<span data-ttu-id="9f2d4-128">Wenn Sie einen Makrogruppennamen für das Argument **Makroname** eingeben, wird das erste Makro in der Makrogruppe in Access ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-128">If you enter a macro group name for the **Macro Name** argument, Access runs the first macro in the macro group.</span></span>

<span data-ttu-id="9f2d4-p105">Diese Aktion ist mit dem Klicken auf **Makro ausführen** auf der Registerkarte **Datenbanktools**, dem Auswählen eines Makros und dem Klicken auf **OK** vergleichbar. Bei diesem Befehl wird das Makro jedoch nur einmal ausgeführt, wohingegen die **AusführenMakro** -Aktion ein Makro so häufig wie gewünscht ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-p105">This action is similar to clicking **Run Macro** on the **Database Tools** tab, selecting a macro, and clicking **OK**. However, this command runs the macro only once, whereas the **RunMacro** action can run a macro as many times as you want.</span></span>


> [!TIP]
> <P><span data-ttu-id="9f2d4-131">[!TIPP] Sie können die Argumente <STRONG>Wiederholbedingung</STRONG> und <STRONG>Wiederholungen</STRONG> verwenden, um festzulegen, wie oft das Makro ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="9f2d4-131">You can use the <STRONG>Repeat Count</STRONG> and <STRONG>Repeat Expression</STRONG> arguments to determine how many times the macro runs:</span></span></P>



  - <span data-ttu-id="9f2d4-132">Wenn Sie beide Argumente leer lassen, wird das Makro einmal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-132">If you leave both arguments blank, the macro runs once.</span></span>

  - <span data-ttu-id="9f2d4-133">Wenn Sie einen Wert für **Wiederholungen** eingeben, aber **Wiederholbedingung** leer lassen, wird das Makro mit der angegebenen Häufigkeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-133">If you enter a number for **Repeat Count** but leave **Repeat Expression** blank, the macro runs the specified number of times.</span></span>

  - <span data-ttu-id="9f2d4-134">Wenn Sie **Wiederholungen** leer lassen, jedoch einen Ausdruck für **Wiederholbedingung** eingeben, wird das Makro ausgeführt, bis der Ausdruck mit **Falsch** ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-134">If you leave **Repeat Count** blank but enter an expression for **Repeat Expression**, the macro runs until the expression evaluates to **False**.</span></span>

  - <span data-ttu-id="9f2d4-135">Wenn Sie Werte für beide Argumente eingeben, wird das Makro mit der Häufigkeit ausgeführt, die in **Wiederholungen** angegeben ist, oder bis **Wiederholbedingung** mit **Falsch** ausgewertet wird, unabhängig davon, was zuerst erfolgt.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-135">If you enter values for both arguments, the macro runs the number of times specified in **Repeat Count** or until **Repeat Expression** evaluates to **False**, whichever occurs first.</span></span>

<span data-ttu-id="9f2d4-p106">Wenn Sie ein Makro ausführen, das die **AusführenMakro** -Aktion enthält, und es die **AusführenMakro** -Aktion erreicht, wird das aufgerufene Makro in Access ausgeführt. Sobald das aufgerufene Makro beendet ist, kehrt Access zum ursprünglichen Makro zurück und führt die nächste Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-p106">When you run a macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called macro. When the called macro has finished, Access returns to the original macro and runs the next action.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="9f2d4-138">Sie können ein Makro in derselben Makrogruppe oder in einer anderen Makrogruppe aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-138">You can call a macro in the same macro group or in another macro group.</span></span></P>
> <LI>
> <P><span data-ttu-id="9f2d4-p107">Sie können Makros schachteln. Sie können also Makro A ausführen, das wiederum Makro B aufruft usw. Sobald das aufgerufene Makro beendet ist, kehrt Access zu dem Makro zurück, das es aufrief, und führt die nächste Aktion in diesem Makro aus.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-p107">You can nest macros. That is, you can run macro A, which in turn calls macro B, and so on. In each case, when the called macro has finished, Access returns to the macro that called it and runs the next action in that macro.</span></span></P></LI></UL>



<span data-ttu-id="9f2d4-142">Verwenden Sie die **RunMacro** -Methode des **DoCmd** -Objekts, um die **AusführenMakro** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9f2d4-142">To run the **RunMacro** action in a Visual Basic for Applications (VBA) module, use the **RunMacro** method of the **DoCmd** object.</span></span>

