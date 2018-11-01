---
title: FestlegenLokaleVar-Makroaktion
TOCTitle: SetLocalVar Macro Action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 299227553481c4f149827c31078111db7b427f7f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886641"
---
# <a name="setlocalvar-macro-action"></a><span data-ttu-id="dc5a3-102">FestlegenLokaleVar-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="dc5a3-102">SetLocalVar Macro Action</span></span>


<span data-ttu-id="dc5a3-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc5a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc5a3-104">Mit der **FestlegenLokaleVar** -Aktion erstellen Sie eine temporäre Variable und legen diese auf einen bestimmten Wert fest.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span>

## <a name="setting"></a><span data-ttu-id="dc5a3-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="dc5a3-105">Setting</span></span>

<span data-ttu-id="dc5a3-106">Die **FestlegenLokaleVar** -Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-106">The **SetLocalVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc5a3-107">Argument</span><span class="sxs-lookup"><span data-stu-id="dc5a3-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="dc5a3-108">Eingabe erforderlich</span><span class="sxs-lookup"><span data-stu-id="dc5a3-108">Required</span></span></p></th>
<th><p><span data-ttu-id="dc5a3-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc5a3-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc5a3-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="dc5a3-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="dc5a3-111">Ja</span><span class="sxs-lookup"><span data-stu-id="dc5a3-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="dc5a3-112">Eine Zeichenfolge, die den Namen der Variablen angibt.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-112">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc5a3-113"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="dc5a3-113"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="dc5a3-114">Ja</span><span class="sxs-lookup"><span data-stu-id="dc5a3-114">Yes</span></span></p></td>
<td><p><span data-ttu-id="dc5a3-115">Ein Ausdruck, der verwendet wird, um den Wert für diese temporäre Variable festzulegen.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-115">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="dc5a3-116">Setzen Sie den Ausdruck mit dem Gleichheitszeichen (=).</span><span class="sxs-lookup"><span data-stu-id="dc5a3-116">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="dc5a3-117">Sie können klicken Sie auf die Schaltfläche <strong>Erstellen</strong> , um den <strong>Ausdrucks-Generator</strong> verwenden, um dieses Argument festzulegen.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-117">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="dc5a3-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dc5a3-118">Remarks</span></span>

<span data-ttu-id="dc5a3-p102">Mit der **FestlegenLokaleVar** -Aktion festgelegte Variablen können nur in dem Makro verwendet werden, in dem sie definiert sind. Verwenden Sie die **[FestlegenTempVar](settempvar-macro-action.md)** -Aktion, um eine Variable zu definieren, die in einem anderen Makro, einer Ereignisprozedur, einem Formular oder einem Bericht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-p102">Variables created by the **SetLocalVar** action can be used only in the macro in which they are defined. Use the **[SetTempVar](settempvar-macro-action.md)** action to define a variable that can be used in another macro, in an event procedure, or on a form or report.</span></span>

<span data-ttu-id="dc5a3-p103">Auf eine erstellte temporäre Variable können Sie in einem Ausdruck verweisen. Wenn Sie beispielsweise die temporäre Variable Gesamtmenge erstellt haben, können Sie diese mithilfe der folgenden Syntax als Steuerelementquelle für ein Textfeld verwenden:</span><span class="sxs-lookup"><span data-stu-id="dc5a3-p103">Once a temporary variable has been created, you can refer to it in an expression. For example, if you created a temporary variable named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.</span></span>

`=[LocalVars]![TotalAmount]`


> [!NOTE]
> <P><span data-ttu-id="dc5a3-123">In einem Makro Daten müssen Sie keinen die LocalVars-Auflistung verwenden, um auf eine Variable verweisen.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-123">In a Data Macro, you do not have to use the LocalVars collection to refer to a variable.</span></span> <span data-ttu-id="dc5a3-124">Angenommen, wenn Sie eine temporäre Variable eines Datenmakros, mit dem Namen TotalAmount erstellt haben, können die Variable als Steuerelementinhalt für ein Textfeld Sie mithilfe der folgenden syntax</span><span class="sxs-lookup"><span data-stu-id="dc5a3-124">For example, if you created a temporary variable in a Data Macro named TotalAmount, you could use the variable as the control source for a text box by using the following syntax</span></span><BR><span data-ttu-id="dc5a3-125">= [TotalAmount]</span><span class="sxs-lookup"><span data-stu-id="dc5a3-125">=[TotalAmount]</span></span></P>


