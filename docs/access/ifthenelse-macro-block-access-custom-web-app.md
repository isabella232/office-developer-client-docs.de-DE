---
title: 'If... Im Anschluss: Makroblock (Access benutzerdefinierte Web app)'
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 18d28dc1-c41f-47c6-b5c7-258d5f877d01
description: Sie können die If Makro-Block bedingt eine Gruppe von Aktionen je nach den Wert eines Ausdrucks ausgeführt.
ms.openlocfilehash: 8ac78ff0eaf22c1d821e306654ebfa8fac4ed34a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790211"
---
# <a name="ifthenelse-macro-block-access-custom-web-app"></a><span data-ttu-id="5b29a-103">If... Im Anschluss: Makroblock (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="5b29a-103">If...Then...Else Macro Block (Access custom web app)</span></span>

<span data-ttu-id="5b29a-104">Mit dem **If** -Makroblock können Sie eine Gruppe von Aktionen je nach Wert eines als Bedingung verwendeten Ausdrucks ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b29a-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="5b29a-p101">[!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="5b29a-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5b29a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b29a-107">Syntax</span></span>

```vb
IfexpressionThen 
 Insert macro actions here ... 
Else Ifexpression  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

## <a name="setting"></a><span data-ttu-id="5b29a-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="5b29a-108">Setting</span></span>

<span data-ttu-id="5b29a-109">Für beide **Wenn** und ** sonst wenn **, die folgenden Argumente erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5b29a-109">For both **If** and ** Else If **, the following arguments are required.</span></span> 
  
|<span data-ttu-id="5b29a-110">**Aktionsargument**</span><span class="sxs-lookup"><span data-stu-id="5b29a-110">**Action argument**</span></span>|<span data-ttu-id="5b29a-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b29a-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5b29a-112">**Expression**</span><span class="sxs-lookup"><span data-stu-id="5b29a-112">**Expression**</span></span> <br/> |<span data-ttu-id="5b29a-113">Die Bedingung, die Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="5b29a-113">The condition that you wish to test.</span></span> <span data-ttu-id="5b29a-114">Es muss ein Ausdruck, der True oder False ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="5b29a-114">It must be an expression that evaluates to True or False.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b29a-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5b29a-115">Remarks</span></span>

<span data-ttu-id="5b29a-116">Bei Auswahl des Makro **If** -Block wird ein TextBox-Steuerelement angezeigt, sodass Sie einen Ausdruck eingeben können, der die Bedingung darstellt, den, die Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="5b29a-116">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test.</span></span> <span data-ttu-id="5b29a-117">Darüber hinaus wird ein Kombinationsfeld mit der Sie eine Makroaktion einfügen können Unterschreitung der Text "End If" automatisch zeigt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b29a-117">In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays.</span></span> <span data-ttu-id="5b29a-118">Die If und End If Klammer einen Bereich, in dem Sie eine Gruppe oder einen Block von Aktionen eingeben können.</span><span class="sxs-lookup"><span data-stu-id="5b29a-118">The If and the End If bracket an area in which you can enter a group, or block, of actions.</span></span> <span data-ttu-id="5b29a-119">Der Block wird ausgeführt, wenn der Ausdruck, den Sie eingeben auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5b29a-119">The block executes only if the expression that you enter is True.</span></span> 
  
<span data-ttu-id="5b29a-120">Um einen anderen Ausdruck auswerten, wenn der erste Ausdruck auf false festgelegt ist, können Sie **Andere Person hinzufügen Wenn** , um einen optionalen **Else If** -Block einzufügen klicken.</span><span class="sxs-lookup"><span data-stu-id="5b29a-120">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block.</span></span> <span data-ttu-id="5b29a-121">Sie müssen einen Ausdruck, der ausgewertet wird auf True oder False, eingeben.</span><span class="sxs-lookup"><span data-stu-id="5b29a-121">You must enter an expression that evaluates to True or False.</span></span> <span data-ttu-id="5b29a-122">-Block wird in diesem Fall nur, wenn der Ausdruck True ist und der erste Ausdruck False ist.</span><span class="sxs-lookup"><span data-stu-id="5b29a-122">In this case, the block executes only if the expression is True and the first expression is False.</span></span> 
  
<span data-ttu-id="5b29a-123">Sie können beliebig viele **Else Wenn** Blöcke beliebig in einem IF blockieren hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5b29a-123">You can add as many **Else If** blocks as you like to an If block.</span></span> 
  
<span data-ttu-id="5b29a-p105">Sie können auf **Add Else** klicken, um einen optionalen **Else** -Block hinzuzufügen. In diesem Fall bilden die unter **Else** eingegebenen Aktionen den **Else** -Block, der nur ausgeführt wird, wenn die darüber angegebenen Aktionen nicht ausgeführt werden. Einem **If** -Block können Sie nur einen **Else** -Block hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5b29a-p105">You can click **Add Else** to insert an optional **Else** block. In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not. You can add a single **Else** block to an **If** block.</span></span> 
  
<span data-ttu-id="5b29a-p106">Im folgenden Codebeispiel werden die Makroaktionen im ersten Block ausgeführt, wenn der Wert von [Status] größer als 0 ist. Wenn der Wert von [Status] nicht größer als 0 ist, wird der Ausdruck nach **Else If** ausgewertet. Die Makroaktionen im **Else If** -Block werden ausgeführt, wenn der Wert von [Status] gleich 0 ist. Wenn letztlich weder der erste noch der zweite Block ausgeführt wird, werden die Aktionen im **Else** -Block ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b29a-p106">In the following code example, the macro actions in the first block execute if the value of [Status] is greater than 0. If the value of [Status] is not greater than 0, the expression that follows the **Else If** is evaluated. The macro actions in the **Else If** block execute if the value of [Status] is equal to 0. Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span> 
  
```vb
If[Status] > 0Then 
 Insert macro actions here ... 
Else If[Status] = 0  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

<span data-ttu-id="5b29a-131">Sie können **Wenn** Blöcke schachteln.</span><span class="sxs-lookup"><span data-stu-id="5b29a-131">You can nest **If** blocks.</span></span> <span data-ttu-id="5b29a-132">Sie sollten einen **If** -Block innerhalb einer **If** -Block schachteln, wenn Sie möchten einen zweiten Ausdruck ausgewertet werden soll, wenn der erste Ausdruck true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5b29a-132">You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True.</span></span> <span data-ttu-id="5b29a-133">Im folgenden Codebeispiel wird führt der innere **If** -Block nur, wenn der Wert der [Status] sowohl größer als 0 *und* größer als 100 ist.</span><span class="sxs-lookup"><span data-stu-id="5b29a-133">In the following code example, the inner **If** block only executes when the value of [Status] is both greater than 0  *and*  greater than 100.</span></span> 
  

