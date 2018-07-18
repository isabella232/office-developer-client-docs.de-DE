---
title: EVALCELL-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Übernimmt einen Verweis auf eine Zelle, die eine benutzerdefinierte Funktion enthält als auch eine oder mehrere Name / Wert-Paare an die benutzerdefinierte Funktion als Argumente (optional) übergeben. Gibt das berechnete Ergebnis der benutzerdefinierten Funktion mit den angegebenen Argumenten und Werten zurück.
ms.openlocfilehash: 03094f644edb29f990f3dda50b0cb4c35e1b07a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796942"
---
# <a name="evalcell-function"></a>EVALCELL Function

Übernimmt einen Verweis auf eine Zelle, die eine benutzerdefinierte Funktion enthält als auch eine oder mehrere Name / Wert-Paare an die benutzerdefinierte Funktion als Argumente (optional) übergeben. Gibt das berechnete Ergebnis der benutzerdefinierten Funktion mit den angegebenen Argumenten und Werten zurück.
  
## <a name="syntax"></a>Syntax

EVALCELL (** *CellRef* **, [** *arg1Name, arg1* **], [** *arg2Name, arg2* **],...) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _cellRef_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Verweis auf die Zelle, die benutzerdefinierte Funktion enthält. Blattübergreifende Verweise sind zulässig.  <br/> |
| _arg1Name_ <br/> |Optional  <br/> |**String** <br/> |Der Name des ersten Arguments, das an die benutzerdefinierte Funktion übergeben wird. Leerzeichen sind zulässig.  <br/> |
| _arg1_ <br/> |Optional  <br/> |**Variiert** <br/> |Der Wert des Parameters _arg1_ .  <br/> |
| _arg2Name_ <br/> |Optional  <br/> |**String** <br/> |Der Name des zweiten Arguments an die benutzerdefinierte Funktion übergeben werden sollen. Leerzeichen sind zulässig.  <br/> |
| _Arg2_ <br/> |Optional  <br/> |**Variiert** <br/> |Der Wert des Parameters _arg2_ .  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

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


