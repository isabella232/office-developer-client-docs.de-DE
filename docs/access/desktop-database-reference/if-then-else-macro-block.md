---
title: Wenn...Dann...Sonst-Makroblock
TOCTitle: If...Then...Else macro block
ms:assetid: 0c4a4b7a-4fdb-9dbc-a94e-939a2ff1c0e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845158(v=office.15)
ms:contentKeyID: 48543188
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: fb6cbd6cc925a3e4841d9e7d6d77332cc36c7a03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291894"
---
# <a name="ifthenelse-macro-block"></a><span data-ttu-id="31a1c-102">Wenn...Dann...Sonst-Makroblock</span><span class="sxs-lookup"><span data-stu-id="31a1c-102">If...Then...Else macro block</span></span>


<span data-ttu-id="31a1c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="31a1c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31a1c-104">Mit dem **If**-Makroblock können Sie eine Gruppe von Aktionen je nach Wert eines als Bedingung verwendeten Ausdrucks ausführen.</span><span class="sxs-lookup"><span data-stu-id="31a1c-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span>

```vb
    If expression Then 
     Insert macro actions here ... 
    Else If expression 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

## <a name="setting"></a><span data-ttu-id="31a1c-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="31a1c-105">Setting</span></span>

<span data-ttu-id="31a1c-106">Für **If** und für **Else If** sind jeweils die folgenden Argumente erforderlich.</span><span class="sxs-lookup"><span data-stu-id="31a1c-106">For both **If** and \*\* Else If\*\*, the following arguments are required.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31a1c-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="31a1c-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="31a1c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31a1c-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31a1c-109"><strong>Ausdruck</strong></span><span class="sxs-lookup"><span data-stu-id="31a1c-109"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="31a1c-110">Die Bedingung, die Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="31a1c-110">The condition that you wish to test.</span></span> <span data-ttu-id="31a1c-111">Dies muss ein Ausdruck sein, der als "Wahr" oder "Falsch" ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="31a1c-111">It must be an expression that evaluates to True or False.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="31a1c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31a1c-112">Remarks</span></span>

<span data-ttu-id="31a1c-p102">Wenn Sie den **If**-Makroblock auswählen, wird ein Textfeld eingeblendet, damit Sie einen Ausdruck zur Darstellung der Bedingung eingeben können, die Sie testen möchten. Darüber hinaus wird ein Kombinationsfeld angezeigt. Sie können darin eine Makroaktion einfügen, unter der der Text "End If" automatisch angezeigt wird. Das "If" und das "End If" klammern einen Bereich ein, in dem Sie eine Gruppe (Block) von Aktionen eingeben können. Der Block wird nur ausgeführt, wenn der eingegebene Ausdruck "Wahr" ist.</span><span class="sxs-lookup"><span data-stu-id="31a1c-p102">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test. In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays. The If and the End If bracket an area in which you can enter a group, or block, of actions. The block executes only if the expression that you enter is True.</span></span>

<span data-ttu-id="31a1c-p103">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block. You must enter an expression that evaluates to True or False. In this case, the block executes only if the expression is True and the first expression is False.</span><span class="sxs-lookup"><span data-stu-id="31a1c-p103">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block. You must enter an expression that evaluates to True or False. In this case, the block executes only if the expression is True and the first expression is False.</span></span>

<span data-ttu-id="31a1c-120">Sie können einem "If"-Block beliebig viele **Else If**-Blöcke hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="31a1c-120">You can add as many **Else If** blocks as you like to an If block.</span></span>

<span data-ttu-id="31a1c-p104">Sie können auf **Add Else** klicken, um einen optionalen **Else** -Block hinzuzufügen. In diesem Fall bilden die unter **Else** eingegebenen Aktionen den **Else** -Block, der nur ausgeführt wird, wenn die darüber angegebenen Aktionen nicht ausgeführt werden. Einem **If** -Block können Sie nur einen **Else** -Block hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="31a1c-p104">You can click **Add Else** to insert an optional **Else** block. In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not. You can add a single **Else** block to an **If** block.</span></span>

<span data-ttu-id="31a1c-124">Im folgenden Codebeispiel werden die Makroaktionen im ersten Block ausgeführt, wenn der Wert von \[Status\] größer als 0 ist.</span><span class="sxs-lookup"><span data-stu-id="31a1c-124">In the following code example, the macro actions in the first block execute if the value of [Status] is greater than 0.</span></span> <span data-ttu-id="31a1c-125">Wenn der Wert von \[Status\] nicht größer als 0 ist, wird der Ausdruck nach **Else If** ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="31a1c-125">If the value of [Status] is not greater than 0, the expression that follows the Else If is evaluated.</span></span> <span data-ttu-id="31a1c-126">Die Makroaktionen im **Else If**-Block werden ausgeführt, wenn der Wert von \[Status\] gleich 0 ist.</span><span class="sxs-lookup"><span data-stu-id="31a1c-126">The macro actions in the Else If block execute if the value of [Status] is equal to 0.</span></span> <span data-ttu-id="31a1c-127">Und schließlich: Wenn weder der erste noch der zweite Block ausgeführt werden, werden die Aktionen im **Else**-Block ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31a1c-127">Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span>

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
    Else If [Status] = 0 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

<span data-ttu-id="31a1c-128">Sie können **If**-Blöcke schachteln.</span><span class="sxs-lookup"><span data-stu-id="31a1c-128">You can nest **If** blocks.</span></span> <span data-ttu-id="31a1c-129">Das Schachteln eines **If**-Blocks in einem **If**-Block sollten Sie erwägen, um einen zweiten Ausdruck auszuwerten, wenn der erste Ausdruck "Wahr" ist.</span><span class="sxs-lookup"><span data-stu-id="31a1c-129">You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True.</span></span> <span data-ttu-id="31a1c-130">Im nachstehenden Codebeispiel wird der innere **If**-Block nur dann ausgewertet, wenn der Wert von \[Status\] größer als "0" *and* größer als "100" ist.</span><span class="sxs-lookup"><span data-stu-id="31a1c-130">In the following code example, the inner If block only executes when the value of [Status] is both greater than 0  and  greater than 100.</span></span>

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
     If [Status] > 100 
     Insert macro actions here ... 
     EndifEnd If
```
