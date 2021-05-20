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
description: Gibt einen nichtuniformierten rationalen B-Spline (NURBS) zurück. Diese Funktion wird in der Zelle E in den NURBSTo-Geometriezeilen verwendet.
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438456"
---
# <a name="nurbs-function"></a>NURBS Function

Gibt einen nichtuniformierten rationalen B-Spline (NURBS) zurück. Diese Funktion wird in der Zelle E in den NURBSTo-Geometriezeilen verwendet.
  
## <a name="syntax"></a>Syntax

NURBS(** *knotLast* **, ** *Degree* **, ** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **, ** *knot1* **, ** *weight1* **, ...) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _knotLast_ <br/> |Erforderlich  <br/> |**Zeichenfolge** <br/> | Der letzte Knoten.  <br/> |
| _degree_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Gradwert des Splines.  <br/> |
| _xType_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Gibt an, wie die  _x-Eingabedaten_ interpretiert werden. Wenn  _xType_ 0 ist, werden alle  _x-Eingabedaten_ als Prozentsatz der Breite interpretiert. Wenn  _xType_ 1 ist, werden alle  _x-Eingabedaten_ als lokale Koordinaten interpretiert.  <br/> |
| _yType_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Gibt an, wie die  _y-Eingabedaten_ interpretiert werden. Wenn  _yType_ 0 ist, werden alle  _y-Eingabedaten_ als Prozentsatz von Height interpretiert. Wenn  _yType_ 1 ist, werden alle  _y-Eingabedaten_ als lokale Koordinaten interpretiert.  <br/> |
| _x1_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine x-Koordinate.  <br/> |
| _y1_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine y-Koordinate.  <br/> |
| _knot1_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Knoten auf dem B-Spline.  <br/> |
| _weight1_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine Breite für das B-Spline.  <br/> |
   
## <a name="remarks"></a>Hinweise

Für jedes  *x-Argument*  muss ein  *y-Argument verwendet*  werden. Andernfalls wird ein Fehler zurückgegeben. 
  
Sie müssen mindestens ein *x*-, *y-,* *Knoten-* und *Gewichtungsargument* angeben. Andernfalls gibt Visio einen Fehler zurück. 
  

