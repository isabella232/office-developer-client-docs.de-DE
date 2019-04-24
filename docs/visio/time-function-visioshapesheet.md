---
title: TIME-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Gibt die von Stunde, Minute und Sekunde dargestellte Zeit zurück.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280997"
---
# <a name="time-function-visioshapesheet"></a>TIME-Funktion (VisioShapeSheet)

Gibt die von _Stunde_, _Minute_und _Sekunde_dargestellte Zeit zurück.
  
## <a name="syntax"></a>Syntax

Uhrzeit (* * *Stunde* * *, * * *Minute* * *, * * *Sekunde* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _hour_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Die Stundenkomponente.  <br/> |
| _minute_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Die Minutenkomponente.  <br/> |
| _second_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Die Sekundenkomponente.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Numerisch
  
## <a name="example-1"></a>Beispiel 1

ZEIT (15, 30, 30)
  
Gibt den Wert für 15:30:30 zurück.
  
## <a name="example-2"></a>Beispiel 2

FORMAT (Zeit (15, 30, 30), "HH: mm")
  
Gibt den Wert für 15:30 zurück.
  
## <a name="example-3"></a>Beispiel 3

TIME(15,30,30) + 8 vs.
  
Gibt den Wert für 23:30:30 zurück.
  

