---
title: CEILING-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
localization_priority: Normal
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Rundet eine Zahl von 0 (null) auf die nächste Instanz von Vielfaches. Wenn Multiple nicht angegeben wurde, wird die Zahl von 0 auf die nächste ganze Zahl gerundet.
ms.openlocfilehash: fa982b44ea4a73e7da614c49a52cd50efd612f20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796578"
---
# <a name="ceiling-function"></a>CEILING Function

Rundet eine Zahl von 0 (null) auf die nächste Instanz von _Vielfaches_. Wenn _mehrere_ nicht angegeben ist, wird die Anzahl von 0 auf die nächste ganze Zahl gerundet. 
  
## <a name="syntax"></a>Syntax

CEILING (** *Anzahl* **, ** *mehrere* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die zu rundende Zahl.  <br/> |
| _mehrere_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Das Vielfache, auf die gerundet werden soll.  <br/> |
   
## <a name="remarks"></a>Hinweise

 _Anzahl_ und _Vielfaches_ müssen die gleichen Vorzeichen oder ein #NUM haben. Fehler wird zurückgegeben. Wenn _Zahl_ oder _mehrere_ auf einen Wert, der ein #VALUE konvertiert werden kann! Fehler wird zurückgegeben. Wenn _Zahl_ oder _mehrere_ 0 ist, ist das Ergebnis 0. 
  
## <a name="example-1"></a>Beispiel 1

CEILING(3.7)
  
Gibt 4 zurück.
  
## <a name="example-2"></a>Beispiel 2

CEILING(-3.7)
  
Gibt -4 zurück.
  
## <a name="example-3"></a>Beispiel 3

CEILING (3.7, 0,25)
  
Gibt 3,75 zurück.
  

