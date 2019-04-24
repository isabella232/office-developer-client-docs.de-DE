---
title: If... Dann... Else-Makro Block (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 18d28dc1-c41f-47c6-b5c7-258d5f877d01
description: Mit dem If -Makroblock können Sie eine Gruppe von Aktionen je nach Wert eines als Bedingung verwendeten Ausdrucks ausführen.
ms.openlocfilehash: 6fe82e2c42f8e5d93cdc26798e7572e32d6cdc7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304263"
---
# <a name="ifthenelse-macro-block-access-custom-web-app"></a>If... Dann... Else-Makro Block (Access Custom Web App)

Mit dem **If** -Makroblock können Sie eine Gruppe von Aktionen je nach Wert eines als Bedingung verwendeten Ausdrucks ausführen. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

```vb
IfexpressionThen 
 Insert macro actions here ... 
Else Ifexpression  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

## <a name="setting"></a>Einstellung

For both **If** and ** Else If **, the following arguments are required. 
  
|**Aktionsargument**|**Beschreibung**|
|:-----|:-----|
|**Ausdruck** <br/> |Die Bedingung, auf die Sie testen möchten. Es muss sich um einen Ausdruck handeln, der mit True oder False ausgewertet wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test. In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays. The If and the End If bracket an area in which you can enter a group, or block, of actions. The block executes only if the expression that you enter is True. 
  
To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block. You must enter an expression that evaluates to True or False. In this case, the block executes only if the expression is True and the first expression is False. 
  
You can add as many **Else If** blocks as you like to an If block. 
  
Sie können auf **Add Else** klicken, um einen optionalen **Else** -Block hinzuzufügen. In diesem Fall bilden die unter **Else** eingegebenen Aktionen den **Else** -Block, der nur ausgeführt wird, wenn die darüber angegebenen Aktionen nicht ausgeführt werden. Einem **If** -Block können Sie nur einen **Else** -Block hinzufügen. 
  
Im folgenden Codebeispiel werden die Makroaktionen im ersten Block ausgeführt, wenn der Wert von [Status] größer als 0 ist. Wenn der Wert von [Status] nicht größer als 0 ist, wird der Ausdruck nach **Else If** ausgewertet. Die Makroaktionen im **Else If** -Block werden ausgeführt, wenn der Wert von [Status] gleich 0 ist. Wenn letztlich weder der erste noch der zweite Block ausgeführt wird, werden die Aktionen im **Else** -Block ausgeführt. 
  
```vb
If[Status] > 0Then 
 Insert macro actions here ... 
Else If[Status] = 0  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

You can nest **If** blocks. You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True. In the following code example, the inner **If** block only executes when the value of [Status] is both greater than 0  *and*  greater than 100. 
  

