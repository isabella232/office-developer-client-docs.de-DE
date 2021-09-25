---
title: NURBS-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251579
ms.localizationpriority: medium
ms.assetid: f34db20d-6501-2026-a5e8-29c4d4cb2405
description: Gibt einen nicht uniform rationalen B-Spline (NURBS) zurück. Diese Funktion wird in der Zelle E in den NURBSTo-Geometriezeilen verwendet.
ms.openlocfilehash: 335b055aef4517a783a7971e9f63bc36fea9dc4c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590184"
---
# <a name="nurbs-function"></a>NURBS Function

Gibt einen nicht uniform rationalen B-Spline (NURBS) zurück. Diese Funktion wird in der Zelle E in den NURBSTo-Geometriezeilen verwendet.
  
## <a name="syntax"></a>Syntax

NURBS(** *knotLast* **, ** *degree* **, ** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **, ** *knot1* **, ** *weight1* **, ...) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _knotLast_ <br/> |Erforderlich  <br/> |**Zeichenfolge** <br/> | Der letzte Knoten.  <br/> |
| _Grad_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Gradwert des Splines.  <br/> |
| _xType_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Gibt an, wie  die x-Eingabedaten interpretiert werden. Wenn  _xType_ 0 ist, werden alle  _x-Eingabedaten_ als Prozentsatz der Breite interpretiert. Wenn  _xType_ 1 ist, werden alle  _x-Eingabedaten_ als lokale Koordinaten interpretiert.  <br/> |
| _yType_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Gibt an, wie die  _y-Eingabedaten_ interpretiert werden. Wenn  _yType_ 0 ist, werden alle  _y-Eingabedaten_ als Prozentsatz der Höhe interpretiert. Wenn  _yType_ 1 ist, werden alle  _y-Eingabedaten_ als lokale Koordinaten interpretiert.  <br/> |
| _x1_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine x-Koordinate.  <br/> |
| _y1_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine y-Koordinate.  <br/> |
| _knot1_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Knoten auf dem B-Spline.  <br/> |
| _weight1_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine Breite für das B-Spline.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Für jedes  *x-Argument*  muss ein  *y-Argument*  vorhanden sein. andernfalls wird ein Fehler zurückgegeben. 
  
Sie müssen mindestens ein *X-,* *Y-,* *Knoten-* und *Gewichtungsargument* angeben. andernfalls gibt Visio einen Fehler zurück. 
  

