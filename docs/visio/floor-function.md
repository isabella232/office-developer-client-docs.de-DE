---
title: FLOOR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Rundet eine Zahl in Richtung 0 (null), auf die nächste ganze Zahl oder auf die nächste Instanz von Multiple.
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346179"
---
# <a name="floor-function"></a>FLOOR Function

Rundet eine Zahl in Richtung 0 (null), auf die nächste ganze Zahl oder auf die nächste Instanz von _Multiple_.
  
## <a name="syntax"></a>Syntax

FLOOR (* * *Number* * *, * * *Multiple* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die zu rundende Zahl.  <br/> |
| _mehrere_ <br/> |Erforderlich  <br/> |**Number** <br/> |Das Vielfache, auf das gerundet werden soll.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zahl
  
## <a name="remarks"></a>Bemerkungen

Wenn _Multiple_ nicht angegeben wird, wird die Zahl in Richtung 0 in die nächste ganze Zahl gerundet. 
  
 _Zahl_ und _mehrere_ müssen die gleichen Zeichen oder ein #NUM! zurückgegeben. Wenn eine oder _mehrere_ _Zahlen_ nicht in einen Wert konvertiert werden können, wird ein #VALUE! zurückgegeben. Wenn eine _Zahl_ oder __ ein Vielfaches 0 ist, ist das Ergebnis 0. 
  
## <a name="example-1"></a>Beispiel 1

BODEN (3.7)
  
Gibt 3 zurück.
  
## <a name="example-2"></a>Beispiel 2

FLOOR (-3,7)
  
Gibt -3 zurück.
  
## <a name="example-3"></a>Beispiel 3

BODEN (3.7, 0,5)
  
Gibt 3,5 zurück.
  

