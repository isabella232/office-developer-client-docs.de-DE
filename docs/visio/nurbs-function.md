---
title: NURBS-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251579
localization_priority: Normal
ms.assetid: f34db20d-6501-2026-a5e8-29c4d4cb2405
description: Gibt einen nicht einheitlichen rationalen B-Spline (NURBS) zurück. Diese Funktion wird in der Zelle "E" in den NURBSTo-Geometrie Zeilen verwendet.
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340124"
---
# <a name="nurbs-function"></a>NURBS Function

Gibt einen nicht einheitlichen rationalen B-Spline (NURBS) zurück. Diese Funktion wird in der Zelle "E" in den NURBSTo-Geometrie Zeilen verwendet.
  
## <a name="syntax"></a>Syntax

NURBS (* * *knotLast* * *, * * *Grad* * *, * * *xType* * *, * * *yType* * *, * * *x1* * *, * * *Y1* * *, * * *Knot1* * *, * * *Gewicht1* * *,...) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _knotLast_ <br/> |Erforderlich  <br/> |**Zeichenfolge** <br/> | Der letzte Knoten.  <br/> |
| _Grad_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Der Gradwert des Splines.  <br/> |
| _xType_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Gibt an, wie die _x_ -Eingabedaten interpretiert werden sollen. Wenn _xType_ 0 ist, werden alle _x_ -Eingabedaten als Prozentsatz der Breite interpretiert. Wenn _xType_ ist, werden alle _x_ -Eingabedaten als lokale Koordinaten interpretiert.  <br/> |
| _yType_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Gibt an, wie die _y_ -Eingabedaten interpretiert werden sollen. Wenn _yType_ 0 ist, werden alle _y_ -Eingabedaten als Prozentsatz der Höhe interpretiert. Wenn _yType_ ist, werden alle _y_ -Eingabedaten als lokale Koordinaten interpretiert.  <br/> |
| _x1_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine x-Koordinate.  <br/> |
| _Y1_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine y-Koordinate.  <br/> |
| _Knot1_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Knoten auf dem B-Spline.  <br/> |
| _Gewicht1_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine Breite für das B-Spline.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Für jedes *x* -Argument muss ein *y* -Argument angegeben werden; Andernfalls wird ein Fehler zurückgegeben. 
  
Sie müssen mindestens ein Argument für *x*, *y*, *Knot* und *Weight* angeben; Andernfalls gibt Visio einen Fehler zurück. 
  

