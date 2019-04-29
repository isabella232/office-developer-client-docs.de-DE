---
title: If... Dann... Else-Makro Block (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 18d28dc1-c41f-47c6-b5c7-258d5f877d01
description: Mit dem If-Makroblock können Sie eine Gruppe von Aktionen je nach Wert eines als Bedingung verwendeten Ausdrucks ausführen.
ms.openlocfilehash: 6fe82e2c42f8e5d93cdc26798e7572e32d6cdc7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434494"
---
# <a name="ifthenelse-macro-block-access-custom-web-app"></a><span data-ttu-id="91675-103">If... Dann... Else-Makro Block (Access Custom Web App)</span><span class="sxs-lookup"><span data-stu-id="91675-103">If...Then...Else Macro Block (Access custom web app)</span></span>

<span data-ttu-id="91675-104">Mit dem **If**-Makroblock können Sie eine Gruppe von Aktionen je nach Wert eines als Bedingung verwendeten Ausdrucks ausführen.</span><span class="sxs-lookup"><span data-stu-id="91675-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="91675-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="91675-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="91675-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="91675-107">Syntax</span></span>

```vb
IfexpressionThen 
 Insert macro actions here ... 
Else Ifexpression  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

## <a name="setting"></a><span data-ttu-id="91675-108">Setting</span><span class="sxs-lookup"><span data-stu-id="91675-108">Setting</span></span>

<span data-ttu-id="91675-109">For both **If** and \*\* Else If \*\*, the following arguments are required.</span><span class="sxs-lookup"><span data-stu-id="91675-109">For both **If** and \*\* Else If \*\*, the following arguments are required.</span></span> 
  
|<span data-ttu-id="91675-110">**Aktionsargument**</span><span class="sxs-lookup"><span data-stu-id="91675-110">**Action argument**</span></span>|<span data-ttu-id="91675-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91675-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="91675-112">**Ausdruck**</span><span class="sxs-lookup"><span data-stu-id="91675-112">**Expression**</span></span> <br/> |<span data-ttu-id="91675-113">Die Bedingung, die Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="91675-113">The condition that you wish to test.</span></span> <span data-ttu-id="91675-114">Dies muss ein Ausdruck sein, der als "Wahr" oder "Falsch" ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="91675-114">It must be an expression that evaluates to True or False.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91675-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91675-115">Remarks</span></span>

<span data-ttu-id="91675-p103">Wenn Sie den **If**-Makroblock auswählen, wird ein Textfeld eingeblendet, damit Sie einen Ausdruck zur Darstellung der Bedingung eingeben können, die Sie testen möchten. Darüber hinaus wird ein Kombinationsfeld angezeigt. Sie können darin eine Makroaktion einfügen, unter der der Text "End If" automatisch angezeigt wird. Das "If" und das "End If" klammern einen Bereich ein, in dem Sie eine Gruppe (Block) von Aktionen eingeben können. Der Block wird nur ausgeführt, wenn der eingegebene Ausdruck "Wahr" ist.</span><span class="sxs-lookup"><span data-stu-id="91675-p103">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test. In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays. The If and the End If bracket an area in which you can enter a group, or block, of actions. The block executes only if the expression that you enter is True.</span></span> 
  
<span data-ttu-id="91675-p104">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block. You must enter an expression that evaluates to True or False. In this case, the block executes only if the expression is True and the first expression is False.</span><span class="sxs-lookup"><span data-stu-id="91675-p104">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block. You must enter an expression that evaluates to True or False. In this case, the block executes only if the expression is True and the first expression is False.</span></span> 
  
<span data-ttu-id="91675-123">Sie können einem "If"-Block beliebig viele **Else If**-Blöcke hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="91675-123">You can add as many **Else If** blocks as you like to an If block.</span></span> 
  
<span data-ttu-id="91675-p105">Sie können auf **Add Else** klicken, um einen optionalen **Else** -Block hinzuzufügen. In diesem Fall bilden die unter **Else** eingegebenen Aktionen den **Else** -Block, der nur ausgeführt wird, wenn die darüber angegebenen Aktionen nicht ausgeführt werden. Einem **If** -Block können Sie nur einen **Else** -Block hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="91675-p105">You can click **Add Else** to insert an optional **Else** block. In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not. You can add a single **Else** block to an **If** block.</span></span> 
  
<span data-ttu-id="91675-p106">Im folgenden Codebeispiel werden die Makroaktionen im ersten Block ausgeführt, wenn der Wert von [Status] größer als 0 ist. Wenn der Wert von [Status] nicht größer als 0 ist, wird der Ausdruck nach **Else If** ausgewertet. Die Makroaktionen im **Else If** -Block werden ausgeführt, wenn der Wert von [Status] gleich 0 ist. Wenn letztlich weder der erste noch der zweite Block ausgeführt wird, werden die Aktionen im **Else** -Block ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91675-p106">In the following code example, the macro actions in the first block execute if the value of [Status] is greater than 0. If the value of [Status] is not greater than 0, the expression that follows the **Else If** is evaluated. The macro actions in the **Else If** block execute if the value of [Status] is equal to 0. Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span> 
  
```vb
If[Status] > 0Then 
 Insert macro actions here ... 
Else If[Status] = 0  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

<span data-ttu-id="91675-p107">You can nest **If** blocks. You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True. In the following code example, the inner **If** block only executes when the value of [Status] is both greater than 0  *and*  greater than 100.</span><span class="sxs-lookup"><span data-stu-id="91675-p107">You can nest **If** blocks. You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True. In the following code example, the inner **If** block only executes when the value of [Status] is both greater than 0  *and*  greater than 100.</span></span> 
  

