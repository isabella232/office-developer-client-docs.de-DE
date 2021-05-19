---
title: POLYLINE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251576
localization_priority: Normal
ms.assetid: 10baeec9-6c9b-b4ba-3138-7d1156a9e056
description: Gibt eine Polylinie zurück. Diese Funktion wird in der Zelle A der PolyLineTo-Geometriezeilen verwendet.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426296"
---
# <a name="polyline-function"></a>POLYLINE Function

Gibt eine Polylinie zurück. Diese Funktion wird in der Zelle A der PolyLineTo-Geometriezeilen verwendet. 
  
## <a name="syntax"></a>Syntax

POLYLINE(** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **...) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _xType_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Gibt an, wie die  _x-Eingabedaten_ interpretiert werden. Wenn _xType_ 0 ist, werden die x-data-Eingaben als Prozentsatz der Breite interpretiert.  Wenn _xType_ 1 ist, werden die x-data-Eingaben als lokale Koordinate interpretiert.   <br/> |
| _yType_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Gibt an, wie die  _y-Eingabedaten_ interpretiert werden. Wenn  _yType_ 0 ist, werden die  _Eingabe-y-Daten_ als Prozentsatz von Height interpretiert. Wenn  _yType_ 1 ist, werden die  _Eingaben y_-data als lokale Koordinate interpretiert.  <br/> |
| _x1_ <br/> |Erforderlich  <br/> |**Number** <br/> | Eine x-Koordinate.  <br/> |
| _y1_ <br/> |Erforderlich  <br/> |**Number** <br/> |Eine y-Koordinate.  <br/> |
   
## <a name="remarks"></a>Hinweise

Für jedes  *x-Argument*  muss ein  *y-Argument verwendet*  werden. Andernfalls wird ein Fehler zurückgegeben. 
  
## <a name="example"></a>Beispiel

POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0) 
  
Gibt ein Rechteck der Dimensionen Breite x Höhe zurück. 
  

