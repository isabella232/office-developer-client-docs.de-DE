---
title: If... Dann... Else-Makroblock (benutzerdefinierte Access-Web-App)
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
# <a name="ifthenelse-macro-block-access-custom-web-app"></a>If... Dann... Else-Makroblock (benutzerdefinierte Access-Web-App)

Mit dem **If**-Makroblock können Sie eine Gruppe von Aktionen je nach Wert eines als Bedingung verwendeten Ausdrucks ausführen. 
  
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

## <a name="setting"></a>Setting

For both **If** and ** Else If **, the following arguments are required. 
  
|**Aktionsargument**|**Beschreibung**|
|:-----|:-----|
|**Ausdruck** <br/> |Die Bedingung, die Sie testen möchten. Dies muss ein Ausdruck sein, der als "Wahr" oder "Falsch" ausgewertet wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie den **If**-Makroblock auswählen, wird ein Textfeld eingeblendet, damit Sie einen Ausdruck zur Darstellung der Bedingung eingeben können, die Sie testen möchten. Darüber hinaus wird ein Kombinationsfeld angezeigt. Sie können darin eine Makroaktion einfügen, unter der der Text "End If" automatisch angezeigt wird. Das "If" und das "End If" klammern einen Bereich ein, in dem Sie eine Gruppe (Block) von Aktionen eingeben können. Der Block wird nur ausgeführt, wenn der eingegebene Ausdruck "Wahr" ist. 
  
To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block. You must enter an expression that evaluates to True or False. In this case, the block executes only if the expression is True and the first expression is False. 
  
Sie können einem "If"-Block beliebig viele **Else If**-Blöcke hinzufügen. 
  
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
  

