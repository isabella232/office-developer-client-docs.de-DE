---
title: SETATREFEXPR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027317
localization_priority: Normal
ms.assetid: c1bd7819-b53b-bff1-69c1-6d78e8fb278b
description: Speichert einen Wert, der durch eine Aktion in der Benutzeroberfläche (UI) oder Automatisierung festgelegt ist.
ms.openlocfilehash: c664717afcc2b81e55495fd1957a86ef1b021d0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798011"
---
# <a name="setatrefexpr-function"></a>SETATREFEXPR Function

Speichert einen Wert, der durch eine Aktion in der Benutzeroberfläche (UI) oder Automatisierung festgelegt ist.
  
## <a name="syntax"></a>Syntax

SETATREFEXPR ([** *Expr_opt* **]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expr_opt_ <br/> |Optional  <br/> |**Variiert** <br/> |Ein Ausdruck, der durch den Wert oder ein Ausdruck, der in der SETATREF-Funktion referenzierten Zelle zugewiesen wird ersetzt wird. Wenn nicht angegeben haben, ist der Anfangswert 0 (null).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert eines SETATREFEXPR-Ausdrucks kann auch über eine SETATREF-Funktion einer anderen Zelle, die auf die Zelle mit dem SETATREFEXPR-Ausdruck verweist, festgelegt werden. 
  
Sie sind nicht auf die Verwendung der SETATREFEXPR-Funktion als Parameter der SETATREF-Funktion beschränkt. 
  
## <a name="example-1"></a>Beispiel 1

Im folgenden Beispiel wird die SETATREFEXPR-Funktion verwendet, um sicherzustellen, dass ein Shape so breit wie der enthaltene Text ist.
  
Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())
  
## <a name="example-2"></a>Beispiel 2

Im folgenden Beispiel wird gezeigt, wie die SETATREFEXPR-Funktion verwendet werden kann, damit Shapes in einem benutzerdefinierten Gitter einrasten. Die SETATREFEXPR-Formeln werden in den Zellen PinX und PinY platziert, sodass der Drehbezugspunkt in dem in User.GridX und User.GridY definierten Gitter einrastet. 
  
User.GridX =2 in
  
User.GridY =2 in
  
PinX = INT (SETATREFEXPR /User.GridX () +.5)\*User.GridX
  
PinY = INT (SETATREFEXPR /User.GridY () +.5)\*User.GridY
  
## <a name="example-3"></a>Beispiel 3

Ein Beispiel zur Verwendung der SETATREFEXPR-Funktion zusammen mit der SETATREF-Funktion finden Sie unter der [SETATREF ](setatref-function.md)-Funktion. 
  

