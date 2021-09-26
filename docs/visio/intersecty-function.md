---
title: INTERSECTY-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251445
ms.localizationpriority: medium
ms.assetid: a298eead-044b-6f40-54c7-e0e6088baa19
description: Gibt die y-Koordinate (im lokalen Koordinatensystem) des Punkts zurück, an dem sich zwei Linien schneiden.
ms.openlocfilehash: 9af2f31df91b0ff4be203a7ad23e680763324aaa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618784"
---
# <a name="intersecty-function"></a>INTERSECTY Function

Gibt  die y-Koordinate (im lokalen Koordinatensystem) des Punkts zurück, an dem sich zwei Linien schneiden. 
  
## <a name="syntax"></a>Syntax

INTERSECTX(** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _x1_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die X-Koordinate eines Punkts in der ersten Linie.  <br/> |
| _y1_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die y-Koordinate eines Punkts in der ersten Zeile.  <br/> |
| _angle1_ <br/> |Erforderlich  <br/> |**Number** <br/> | Der Wert der Zelle Winkel für die erste Linie.  <br/> |
| _x2_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die X-Koordinate eines Punkts in der zweiten Zeile.  <br/> |
| _y2_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die y-Koordinate eines Punkts in der zweiten Zeile.  <br/> |
| _angle2_ <br/> |Erforderlich  <br/> |**Number** <br/> |Der Wert der Zelle Winkel für die zweite Linie.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zahl
  
## <a name="remarks"></a>Bemerkungen

Die einzelnen Linien werden als ein Punkt (*x,y*) und ein Winkel definiert. 
  
Von Microsoft Visio wird diese Funktion in der Zelle PinY eines Shapes verwendet, das an eine gedrehte Führungslinie geklebt ist. 
  
Weisen die Linien keinen Schnittpunkt auf, gibt die Funktion einen Nullteilungsfehler (#DIV/0!) zurück. Visio ignoriert die Fehlermeldung und stellt den letzten bekannten Wert für den Punkt wieder her. 
  
## <a name="example"></a>Beispiel

INTERSECTY(VertGuide! PinX, VertGuide! PinY, VertGuide! Angle, HorzGuide! PinX, HorzGuide! PinY, HorzGuide! Winkel) 
  
Gibt  die y-Koordinate des Schnittpunkts von VertGuide und HorzGuide in Seiteneinheiten zurück. 
  

