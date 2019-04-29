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
description: Rundet eine Zahl von 0 (null) zur nächsten Instanz von Multiple ab. Wenn mehrere nicht angegeben ist, wird die Zahl von 0 auf die nächste ganze Zahl gerundet.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404127"
---
# <a name="ceiling-function"></a>CEILING Function

Rundet eine Zahl von 0 (null) zur nächsten Instanz von _Multiple_ab. Wenn _mehrere_ nicht angegeben ist, wird die Zahl von 0 auf die nächste ganze Zahl gerundet. 
  
## <a name="syntax"></a>Syntax

Obergrenze (* * *Number* * *, * * *Multiple* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die zu rundende Zahl.  <br/> |
| _mehrere_ <br/> |Erforderlich  <br/> |**Number** <br/> |Das Vielfache, auf das gerundet werden soll.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 _Zahl_ und _mehrere_ müssen die gleichen Zeichen oder ein #NUM! zurückgegeben. Wenn eine oder _mehrere_ _Zahlen_ nicht in einen Wert konvertiert werden können, wird ein #VALUE! zurückgegeben. Wenn eine _Zahl_ oder __ ein Vielfaches 0 ist, ist das Ergebnis 0. 
  
## <a name="example-1"></a>Beispiel 1

OBERGRENZE (3.7)
  
Gibt 4 zurück.
  
## <a name="example-2"></a>Beispiel 2

DECKE (-3,7)
  
Gibt -4 zurück.
  
## <a name="example-3"></a>Beispiel 3

OBERGRENZE (3.7, 0,25)
  
Gibt 3,75 zurück.
  

