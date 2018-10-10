---
title: Wenn...Dann...Sonst-Makroblock
TOCTitle: If...Then...Else Macro Block
ms:assetid: 0c4a4b7a-4fdb-9dbc-a94e-939a2ff1c0e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845158(v=office.15)
ms:contentKeyID: 48543188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 79e5379ad2c50eff3ddf12b597defc7b85cefb39
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476057"
---
# <a name="ifthenelse-macro-block"></a><span data-ttu-id="ac8d4-102">Wenn...Dann...Sonst-Makroblock</span><span class="sxs-lookup"><span data-stu-id="ac8d4-102">If...Then...Else Macro Block</span></span>


<span data-ttu-id="ac8d4-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac8d4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ac8d4-104">Mit dem **If** -Makroblock können Sie eine Gruppe von Aktionen je nach Wert eines als Bedingung verwendeten Ausdrucks ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac8d4-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span>

```vb
    If expression Then 
     Insert macro actions here ... 
    Else If expression 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

## <a name="setting"></a><span data-ttu-id="ac8d4-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="ac8d4-105">Setting</span></span>

<span data-ttu-id="ac8d4-106">**Wenn** sowohl **Sonst wenn**sind die folgenden Argumente erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ac8d4-106">For both **If** and **Else If**, the following arguments are required.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ac8d4-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="ac8d4-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ac8d4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac8d4-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac8d4-109"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="ac8d4-109"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="ac8d4-110">Die Bedingung, die Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="ac8d4-110">The condition that you wish to test.</span></span> <span data-ttu-id="ac8d4-111">Es muss ein Ausdruck, der True oder False ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="ac8d4-111">It must be an expression that evaluates to True or False.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ac8d4-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ac8d4-112">Remarks</span></span>

<span data-ttu-id="ac8d4-p102">Wenn Sie den If-Makroblock auswählen, wird ein Textfeld angezeigt, sodass Sie einen Ausdruck eingeben können, der die Bedingung darstellt, auf die Sie testen möchten. Zudem wird ein Kombinationsfeld angezeigt, in dem Sie eine Makroaktion einfügen können. Darunter wird automatisch der Text "End If" angezeigt. "If" und "End If" begrenzen einen Bereich, in dem Sie eine Gruppe oder einen Block von Aktionen eingeben können. Der Block wird nur ausgeführt, wenn der von Ihnen eingegebene Ausdruck True ist.</span><span class="sxs-lookup"><span data-stu-id="ac8d4-p102">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test. In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays. The If and the End If bracket an area in which you can enter a group, or block, of actions. The block executes only if the expression that you enter is True.</span></span>

<span data-ttu-id="ac8d4-117">Um einen anderen Ausdruck auswerten, wenn der erste Ausdruck auf false festgelegt ist, können Sie **Andere Person hinzufügen Wenn** , um einen optionalen **Else If** -Block einzufügen klicken.</span><span class="sxs-lookup"><span data-stu-id="ac8d4-117">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block.</span></span> <span data-ttu-id="ac8d4-118">Sie müssen einen Ausdruck, der ausgewertet wird auf True oder False, eingeben.</span><span class="sxs-lookup"><span data-stu-id="ac8d4-118">You must enter an expression that evaluates to True or False.</span></span> <span data-ttu-id="ac8d4-119">-Block wird in diesem Fall nur, wenn der Ausdruck True ist und der erste Ausdruck False ist.</span><span class="sxs-lookup"><span data-stu-id="ac8d4-119">In this case, the block executes only if the expression is True and the first expression is False.</span></span>

<span data-ttu-id="ac8d4-120">In einem If-Block können Sie beliebig viele Else If-Blöcke eingeben.</span><span class="sxs-lookup"><span data-stu-id="ac8d4-120">You can add as many **Else If** blocks as you like to an If block.</span></span>

<span data-ttu-id="ac8d4-p104">Sie können auf **Add Else** klicken, um einen optionalen **Else** -Block hinzuzufügen. In diesem Fall bilden die unter **Else** eingegebenen Aktionen den **Else** -Block, der nur ausgeführt wird, wenn die darüber angegebenen Aktionen nicht ausgeführt werden. Einem **If** -Block können Sie nur einen **Else** -Block hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ac8d4-p104">You can click **Add Else** to insert an optional **Else** block. In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not. You can add a single **Else** block to an **If** block.</span></span>

<span data-ttu-id="ac8d4-124">Im folgenden Codebeispiel wird die Makroaktionen in der erste Block ausgeführt werden, wenn der Wert der \[Status\] größer als 0 ist.</span><span class="sxs-lookup"><span data-stu-id="ac8d4-124">In the following code example, the macro actions in the first block execute if the value of \[Status\] is greater than 0.</span></span> <span data-ttu-id="ac8d4-125">Wenn der Wert der \[Status\] ist nicht größer als 0 ist, wird der Ausdruck, der die **Sonst wenn** befolgt ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="ac8d4-125">If the value of \[Status\] is not greater than 0, the expression that follows the **Else If** is evaluated.</span></span> <span data-ttu-id="ac8d4-126">Die Makroaktionen im **Else If** -Block ausgeführt werden, wenn der Wert der \[Status\] ist gleich 0.</span><span class="sxs-lookup"><span data-stu-id="ac8d4-126">The macro actions in the **Else If** block execute if the value of \[Status\] is equal to 0.</span></span> <span data-ttu-id="ac8d4-127">Wenn letztlich weder der erste noch der zweite Block ausgeführt wird, werden die Aktionen im **Else** -Block ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac8d4-127">Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span>

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
    Else If [Status] = 0 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

<span data-ttu-id="ac8d4-128">Sie können **Wenn** Blöcke schachteln.</span><span class="sxs-lookup"><span data-stu-id="ac8d4-128">You can nest **If** blocks.</span></span> <span data-ttu-id="ac8d4-129">Sie sollten einen **If** -Block innerhalb einer **If** -Block schachteln, wenn Sie möchten einen zweiten Ausdruck ausgewertet werden soll, wenn der erste Ausdruck true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ac8d4-129">You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True.</span></span> <span data-ttu-id="ac8d4-130">Im folgenden Codebeispiel wird der innere **If** -Block nur wird ausgeführt, wenn der Wert der \[Status\] ist sowohl größer als 0 *und* größer als 100.</span><span class="sxs-lookup"><span data-stu-id="ac8d4-130">In the following code example, the inner **If** block only executes when the value of \[Status\] is both greater than 0 *and* greater than 100.</span></span>

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
     If [Status] > 100 
     Insert macro actions here ... 
     EndifEnd If
```
