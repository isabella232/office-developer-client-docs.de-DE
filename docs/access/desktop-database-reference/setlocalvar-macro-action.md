---
title: SetLocalVar-Makroaktion
TOCTitle: SetLocalVar macro action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 091b9717b9a2e35cfc8d0c8555e28570628065ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314588"
---
# <a name="setlocalvar-macro-action"></a><span data-ttu-id="29bb5-102">SetLocalVar-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="29bb5-102">SetLocalVar macro action</span></span>

<span data-ttu-id="29bb5-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="29bb5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="29bb5-104">Mit der **FestlegenLokaleVar**-Aktion erstellen Sie eine temporäre Variable und legen diese auf einen bestimmten Wert fest.</span><span class="sxs-lookup"><span data-stu-id="29bb5-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span>

## <a name="setting"></a><span data-ttu-id="29bb5-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="29bb5-105">Setting</span></span>

<span data-ttu-id="29bb5-106">Die **FestlegenLokaleVar**-Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29bb5-106">The **SetLocalVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="29bb5-107">Argument</span><span class="sxs-lookup"><span data-stu-id="29bb5-107">argument</span></span></p></th>
<th><p><span data-ttu-id="29bb5-108">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="29bb5-108">Required</span></span></p></th>
<th><p><span data-ttu-id="29bb5-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29bb5-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29bb5-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="29bb5-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="29bb5-111">Ja</span><span class="sxs-lookup"><span data-stu-id="29bb5-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="29bb5-112">Eine Zeichenfolge, die den Namen der Variablen angibt.</span><span class="sxs-lookup"><span data-stu-id="29bb5-112">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29bb5-113"><strong>Ausdruck</strong></span><span class="sxs-lookup"><span data-stu-id="29bb5-113"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="29bb5-114">Ja</span><span class="sxs-lookup"><span data-stu-id="29bb5-114">Yes</span></span></p></td>
<td><p><span data-ttu-id="29bb5-115">Ein Ausdruck, mit dem der Wert für diese temporäre Variable festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="29bb5-115">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="29bb5-116">Stellen Sie dem Ausdruck kein Gleichheitszeichen (=) voran.</span><span class="sxs-lookup"><span data-stu-id="29bb5-116">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="29bb5-117">Sie können auf die Schaltfläche <strong>Erstellen</strong> klicken, um das Argument mithilfe des <strong>Ausdrucks-Generators</strong> festzulegen.</span><span class="sxs-lookup"><span data-stu-id="29bb5-117">You can click the <strong>Build</strong> button  to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="29bb5-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29bb5-118">Remarks</span></span>

<span data-ttu-id="29bb5-p102">Mit der **FestlegenLokaleVar** -Aktion festgelegte Variablen können nur in dem Makro verwendet werden, in dem sie definiert sind. Verwenden Sie die **[FestlegenTempVar](settempvar-macro-action.md)** -Aktion, um eine Variable zu definieren, die in einem anderen Makro, einer Ereignisprozedur, einem Formular oder einem Bericht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="29bb5-p102">Variables created by the **SetLocalVar** action can be used only in the macro in which they are defined. Use the **[SetTempVar](settempvar-macro-action.md)** action to define a variable that can be used in another macro, in an event procedure, or on a form or report.</span></span>

<span data-ttu-id="29bb5-p103">Once a temporary variable has been created, you can refer to it in an expression. For example, if you created a temporary variable named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.</span><span class="sxs-lookup"><span data-stu-id="29bb5-p103">Once a temporary variable has been created, you can refer to it in an expression. For example, if you created a temporary variable named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.</span></span>

`=[LocalVars]![TotalAmount]`

> [!NOTE]
> <span data-ttu-id="29bb5-123">In einem Datenmakro müssen Sie nicht die LocalVars-Sammlung verwenden, um auf eine Variable zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="29bb5-123">In a Data Macro, you do not have to use the LocalVars collection to refer to a variable.</span></span> <span data-ttu-id="29bb5-124">Wenn Sie beispielsweise eine temporäre Variable namens "TotalAmount" in einem Datenmakro verwenden, können Sie die Variable über die folgende Syntax als Steuerelementquelle für ein Textfeld verwenden: `=[TotalAmount]`.</span><span class="sxs-lookup"><span data-stu-id="29bb5-124">For example, if you created a temporary variable in a Data Macro named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.</span></span>

