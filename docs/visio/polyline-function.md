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
description: Gibt eine Polylinie zurück. Diese Funktion wird in einer Zelle mit PolyLineTo-Geometrie Zeilen verwendet.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348279"
---
# <a name="polyline-function"></a>POLYLINE Function

Gibt eine Polylinie zurück. Diese Funktion wird in einer Zelle mit PolyLineTo-Geometrie Zeilen verwendet. 
  
## <a name="syntax"></a>Syntax

POLYLINIE (* * *xType* * *, * * *yType* * *, * * *x1* * *, * * *Y1* * *...) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _xType_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Gibt an, wie die _x_ -Eingabedaten interpretiert werden sollen. Wenn _xType_ 0 ist, werden die Eingabe- _x_-Daten als Prozentsatz der Breite interpretiert. Wenn _xType_ 1 ist, werden die Eingabe- _x_-Daten als lokale Koordinate interpretiert.  <br/> |
| _yType_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Gibt an, wie die _y_-Eingabedaten interpretiert werden sollen. Wenn _yType_ 0 ist, werden die Eingabe- _y_-Daten als Prozentsatz der Höhe interpretiert. Wenn _yType_ 1 ist, werden die Eingabe- _y_-Daten als lokale Koordinate interpretiert.  <br/> |
| _x1_ <br/> |Erforderlich  <br/> |**Number** <br/> | Eine _x_-Koordinate.  <br/> |
| _Y1_ <br/> |Erforderlich  <br/> |**Number** <br/> |_Y_-Koordinate.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Für jedes *x* -Argument muss ein *y* -Argument angegeben werden; Andernfalls wird ein Fehler zurückgegeben. 
  
## <a name="example"></a>Beispiel

POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0) 
  
Gibt ein Rechteck der Dimensionen Breite x Höhe zurück. 
  

