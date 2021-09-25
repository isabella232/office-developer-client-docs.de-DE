---
title: ARG-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: Gibt ein Argument an, das die aufrufende Zelle an eine benutzerdefinierte Funktion übergeben kann, sowie den Standardwert, der von der benutzerdefinierten Funktion zurückgegeben wird, wenn die aufrufende Zelle keinen Wert für das Argument übergibt. Gibt den durch die aufrufende Zelle und den entsprechenden argName-Parameter angegebenen Wert zurück.
ms.openlocfilehash: df1e3106eb624064be48bed76201dae6fe40e3cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628857"
---
# <a name="arg-function"></a>ARG Function

Gibt ein Argument an, das die aufrufende Zelle an eine benutzerdefinierte Funktion übergeben kann, sowie den Standardwert, der von der benutzerdefinierten Funktion zurückgegeben wird, wenn die aufrufende Zelle keinen Wert für das Argument übergibt. Gibt den durch die aufrufende Zelle und den entsprechenden argName-Parameter angegebenen Wert zurück.
  
## <a name="syntax"></a>Syntax

ARG(***argName** _,[ _ *_defaultValue_** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _argName_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name eines Arguments, das die aufrufende Zelle an die Funktion übergeben kann.  <br/> |
| _Standardwert_ <br/> |Optional  <br/> |**Numeric** <br/> |Der von ARG zurückgegebene Wert, wenn die aufrufende Zelle keinen Wert für den  _argName-Parameter_ übergeben hat.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Als Entwickler von Shapes können Sie benutzerdefinierte Funktionen erstellen, indem Sie einen Ausdruck in eine Zelle einfügen und diesen Ausdruck von anderen Zellen aus aufrufen. Der Ausdruck kann literale Zeichenfolgen, ShapeSheet-Funktionen und Zellbezüge enthalten. Außerdem kann der Ausdruck bestimmte Argumente enthalten, die von der aufrufenden Zelle übergeben werden. 
  
Die aufrufende Zelle gibt die Zelle mit der benutzerdefinierten Funktion sowie Argumente an, die an die Funktion übergeben werden sollen. Die Ausdruckszelle wird ausgewertet, und das Ergebnis wird an die aufrufende Zelle zurückgegeben.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird gezeigt, wie Sie mit der ARG-Funktion in Verbindung mit der EVALCELL-Funktion den Mittelwert aus einer Menge von drei Werte finden. 
  
Fügen Sie in die Ausdruckszelle den folgenden Code ein, der die benutzerdefinierte Funktion definiert: 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

Fügen Sie in die aufrufenden Zellen den folgenden Code ein, der die benutzerdefinierte Funktion aufruft:
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


