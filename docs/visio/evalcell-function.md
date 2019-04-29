---
title: EVALCELL-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Ruft einen Verweis auf eine Zelle ab, die eine benutzerdefinierte Funktion enthält, sowie ein oder mehrere Name-Wert-Paare, die an die benutzerdefinierte Funktion als Argumente übergeben werden (optional). Gibt das berechnete Ergebnis der benutzerdefinierten Funktion bei den angegebenen Argumenten und Werten zurück.
ms.openlocfilehash: 4ad6645862d620a36b90e4f46d09588d7e83fcc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418904"
---
# <a name="evalcell-function"></a>EVALCELL Function

Ruft einen Verweis auf eine Zelle ab, die eine benutzerdefinierte Funktion enthält, sowie ein oder mehrere Name-Wert-Paare, die an die benutzerdefinierte Funktion als Argumente übergeben werden (optional). Gibt das berechnete Ergebnis der benutzerdefinierten Funktion bei den angegebenen Argumenten und Werten zurück.
  
## <a name="syntax"></a>Syntax

EVALCELL (* * *cellRef* * *, [* * *arg1Name, arg1* * *], [* * *arg2Name, arg2* * *],...) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _cellRef_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Bezug auf die Zelle, die die benutzerdefinierte Funktion enthält. Tabellenübergreifende Bezüge sind zulässig.  <br/> |
| _arg1Name_ <br/> |Optional  <br/> |**String** <br/> |Der Name des ersten Arguments, das an die benutzerdefinierte Funktion übergeben wird. Leerzeichen sind zulässig.  <br/> |
| _arg1_ <br/> |Optional  <br/> |**Variiert** <br/> |Wert des _arg1_ -Parameters.  <br/> |
| _arg2Name_ <br/> |Optional  <br/> |**String** <br/> |Der Name des zweiten Arguments, das an die benutzerdefinierte Funktion übergeben werden soll. Leerzeichen sind zulässig.  <br/> |
| _arg2_ <br/> |Optional  <br/> |**Variiert** <br/> |Wert des _arg2_ -Parameters.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zahl
  
## <a name="remarks"></a>Bemerkungen

In der aufrufenden Zelle muss nicht jedes von der benutzerdefinierten Funktion verwendete Argument angegeben werden. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird gezeigt, wie Sie mit der EVALCELL-Funktion in Verbindung mit der ARG-Funktion den Mittelwert aus einer Menge von drei Werte finden. 
  
Fügen Sie in die Ausdruckszelle den folgenden Code ein, der die benutzerdefinierte Funktion definiert: 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

Fügen Sie in die aufrufenden Zellen den folgenden Code ein, der die benutzerdefinierte Funktion aufruft:
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


