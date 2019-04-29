---
title: INTERSECTY-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251445
localization_priority: Normal
ms.assetid: a298eead-044b-6f40-54c7-e0e6088baa19
description: Gibt die y-Koordinate (im lokalen Koordinatensystem) des Punkts zurück, an dem sich zwei Linien überschneiden.
ms.openlocfilehash: 6fcd06e7086d52b9c45f1deb9d4c191f1a7b1fd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426100"
---
# <a name="intersecty-function"></a>INTERSECTY Function

Gibt die *y* -Koordinate (im lokalen Koordinatensystem) des Punkts zurück, an dem sich zwei Linien überschneiden. 
  
## <a name="syntax"></a>Syntax

INTERSECTX-(* * *x1* * *, * * *Y1* * *, * * *angle1* * *, * * *x2* * *, * * *Y2* * *, * * *angle2* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _x1_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die _x_-Koordinate eines Punkts in der ersten Leitung.  <br/> |
| _Y1_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die _y_-Koordinate eines Punkts in der ersten Leitung.  <br/> |
| _angle1_ <br/> |Erforderlich  <br/> |**Number** <br/> | Der Wert der Zelle Winkel für die erste Linie.  <br/> |
| _x2_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die _x_-Koordinate eines Punkts in der zweiten Reihe.  <br/> |
| _Y2_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die _y_-Koordinate eines Punkts in der zweiten Leitung.  <br/> |
| _angle2_ <br/> |Erforderlich  <br/> |**Number** <br/> |Der Wert der Zelle Winkel für die zweite Linie.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zahl
  
## <a name="remarks"></a>Bemerkungen

Die einzelnen Linien werden als ein Punkt (*x,y*) und ein Winkel definiert. 
  
Von Microsoft Visio wird diese Funktion in der Zelle PinY eines Shapes verwendet, das an eine gedrehte Führungslinie geklebt ist. 
  
Weisen die Linien keinen Schnittpunkt auf, gibt die Funktion einen Nullteilungsfehler (#DIV/0!) zurück. Visio ignoriert die Fehlermeldung und stellt den letzten bekannten Wert für den Punkt wieder her. 
  
## <a name="example"></a>Beispiel

INTERSECTy (VertFL! PinX, VertFL! PinY, VertFL! Angle, Horzfl! PinX, Horzfl! PinY, Horzfl! Winkel 
  
Gibt die *y* -Koordinate des Schnittpunkts von VertFL und horzfl in Seiteneinheiten zurück. 
  

