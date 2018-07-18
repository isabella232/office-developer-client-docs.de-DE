---
title: 'If... Im Anschluss: Makroblock (Access benutzerdefinierte Web app)'
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 18d28dc1-c41f-47c6-b5c7-258d5f877d01
description: Mit dem If -Makroblock können Sie eine Gruppe von Aktionen je nach Wert eines als Bedingung verwendeten Ausdrucks ausführen.
ms.openlocfilehash: 8ac78ff0eaf22c1d821e306654ebfa8fac4ed34a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790211"
---
# <a name="ifthenelse-macro-block-access-custom-web-app"></a>If... Im Anschluss: Makroblock (Access benutzerdefinierte Web app)

Mit dem **If** -Makroblock können Sie eine Gruppe von Aktionen je nach Wert eines als Bedingung verwendeten Ausdrucks ausführen. 
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
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

Für beide **Wenn** und ** sonst wenn **, die folgenden Argumente erforderlich sind. 
  
|**Aktionsargument**|**Beschreibung**|
|:-----|:-----|
|**Expression** <br/> |Die Bedingung, die Sie testen möchten. Es muss ein Ausdruck, der True oder False ausgewertet wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie den If-Makroblock auswählen, wird ein Textfeld angezeigt, sodass Sie einen Ausdruck eingeben können, der die Bedingung darstellt, auf die Sie testen möchten. Zudem wird ein Kombinationsfeld angezeigt, in dem Sie eine Makroaktion einfügen können. Darunter wird automatisch der Text "End If" angezeigt. "If" und "End If" begrenzen einen Bereich, in dem Sie eine Gruppe oder einen Block von Aktionen eingeben können. Der Block wird nur ausgeführt, wenn der von Ihnen eingegebene Ausdruck True ist. 
  
Um einen anderen Ausdruck auswerten, wenn der erste Ausdruck auf false festgelegt ist, können Sie **Andere Person hinzufügen Wenn** , um einen optionalen **Else If** -Block einzufügen klicken. Sie müssen einen Ausdruck, der ausgewertet wird auf True oder False, eingeben. -Block wird in diesem Fall nur, wenn der Ausdruck True ist und der erste Ausdruck False ist. 
  
In einem If-Block können Sie beliebig viele Else If-Blöcke eingeben. 
  
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

Sie können **Wenn** Blöcke schachteln. Sie sollten einen **If** -Block innerhalb einer **If** -Block schachteln, wenn Sie möchten einen zweiten Ausdruck ausgewertet werden soll, wenn der erste Ausdruck true festgelegt ist. Im folgenden Codebeispiel wird führt der innere **If** -Block nur, wenn der Wert der [Status] sowohl größer als 0 *und* größer als 100 ist. 
  

