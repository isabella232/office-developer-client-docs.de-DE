---
title: POLYLINE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251576
ms.localizationpriority: medium
ms.assetid: 10baeec9-6c9b-b4ba-3138-7d1156a9e056
description: Gibt eine Polylinie zurück. Diese Funktion wird in der Zelle A der Zeilen PolyLineTo verwendet.
ms.openlocfilehash: 9d14021acd8e2a8086d44e7cf59a766ce41a6dcc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608088"
---
# <a name="polyline-function"></a>POLYLINE Function

Gibt eine Polylinie zurück. Diese Funktion wird in der Zelle A der Zeilen PolyLineTo verwendet. 
  
## <a name="syntax"></a>Syntax

POLYLINE(** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **...) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _xType_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Gibt an, wie  die x-Eingabedaten interpretiert werden. Wenn  _xType_ 0 ist, werden die  _x-Daten_ als Prozentsatz der Breite interpretiert. Wenn _xType_ 1 ist, werden die x-Data-Eingaben als lokale Koordinate interpretiert.   <br/> |
| _yType_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Gibt an, wie die  _y-Eingabedaten_ interpretiert werden. Wenn  _yType_ 0 ist, werden die  _Eingabedaten "y_-" als Prozentsatz der Höhe interpretiert. Wenn  _yType_ 1 ist, werden die  _Eingabedaten "y_-" als lokale Koordinate interpretiert.  <br/> |
| _x1_ <br/> |Erforderlich  <br/> |**Number** <br/> | Eine _X-Koordinate._  <br/> |
| _y1_ <br/> |Erforderlich  <br/> |**Number** <br/> |Eine y-Koordinate.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Für jedes  *x-Argument*  muss ein  *y-Argument*  vorhanden sein. andernfalls wird ein Fehler zurückgegeben. 
  
## <a name="example"></a>Beispiel

POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0) 
  
Gibt ein Rechteck der Dimensionen Breite x Höhe zurück. 
  

