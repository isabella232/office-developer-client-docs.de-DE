---
title: ARG-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: Gibt ein Argument, das die aufrufende Zelle an eine benutzerdefinierte Funktion übergeben kann als auch der Standardwert von der benutzerdefinierten Funktion zurückgegeben, wenn die aufrufende Zelle keinen in einen Wert für das Argument übergeben wird. Gibt den Wert der aufrufenden Zelle und der entsprechende ArgName-Parameter angegeben wird.
ms.openlocfilehash: 3d0e126e0fa075ff2a07773197c1973e6b0249d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796428"
---
# <a name="arg-function"></a>ARG Function

Gibt ein Argument, das die aufrufende Zelle an eine benutzerdefinierte Funktion übergeben kann als auch der Standardwert von der benutzerdefinierten Funktion zurückgegeben, wenn die aufrufende Zelle keinen in einen Wert für das Argument übergeben wird. Gibt den Wert der aufrufenden Zelle und der entsprechende ArgName-Parameter angegeben wird.
  
## <a name="syntax"></a>Syntax

ARG (** *ArgName* **, [** *DefaultValue* **]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _argName_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name eines Arguments, das die aufrufende Zelle an die Funktion übergeben kann.  <br/> |
| _Standardwert_ <br/> |Optional  <br/> |**Numerisch** <br/> |Der Wert, der von ARG zurückgegeben, wenn die aufrufende Zelle nicht in einen Wert für den _ArgName_ -Parameter übergeben hat.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Als Entwickler von Shapes können Sie benutzerdefinierte Funktionen erstellen, indem Sie einen Ausdruck in eine Zelle einfügen und diesen Ausdruck von anderen Zellen aus aufrufen. Der Ausdruck kann literale Zeichenfolgen, ShapeSheet-Funktionen und Zellbezüge enthalten. Außerdem kann der Ausdruck bestimmte Argumente enthalten, die von der aufrufenden Zelle übergeben werden. 
  
Die aufrufende Zelle gibt die Zelle, die enthält die benutzerdefinierte Funktion als auch für alle Argumente, die an die Funktion übergeben werden sollen. Die Ausdruckszelle ausgewertet und das Ergebnis an die aufrufende Zelle zurückgegeben.
  
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


