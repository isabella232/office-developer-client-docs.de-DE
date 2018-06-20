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
description: Gibt die y-Koordinate (im lokalen Koordinatensystem) des Punkts, in dem zwei Linien überschneiden.
ms.openlocfilehash: c3c0e9afef317ed4c647f1d236c4c3a29c6cdaa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797214"
---
# <a name="intersecty-function"></a>INTERSECTY Function

Gibt die *y* -Koordinate (im lokalen Koordinatensystem) des Punkts, in dem zwei Linien überschneiden. 
  
## <a name="syntax"></a>Syntax

INTERSECTX (** *X1* **, ** *y1* **, ** *Winkel1* **, ** *X2* **, ** *y2* **, ** *Winkel2* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _x1_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die _X_-Koordinate eines Punkts auf der ersten Linie.  <br/> |
| _Y1_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die _y_-Koordinate eines Punkts auf der ersten Linie.  <br/> |
| _Winkel1_ <br/> |Erforderlich  <br/> |**Nummer** <br/> | Der Wert der Zelle Winkel für die erste Linie.  <br/> |
| _x2_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die _X_-Koordinate eines Punkts auf der zweiten Linie.  <br/> |
| _Y2_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die _y_-Koordinate eines Punkts auf der zweiten Linie.  <br/> |
| _Winkel2_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Der Wert der Zelle Winkel für die zweite Linie.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zahl
  
## <a name="remarks"></a>Hinweise

Jede Zeile wird als ein Punkt (*X, y*) und ein Winkel definiert. 
  
Von Microsoft Visio wird diese Funktion in der Zelle PinY eines Shapes verwendet, das an eine gedrehte Führungslinie geklebt ist. 
  
Weisen die Linien keinen Schnittpunkt auf, gibt die Funktion einen Nullteilungsfehler (#DIV/0!) zurück. Visio ignoriert die Fehlermeldung und stellt den letzten bekannten Wert für den Punkt wieder her. 
  
## <a name="example"></a>Beispiel

INTERSECTY (VertFL! DrehbezX VertFL! PinY, VertFL! Winkel, HorzFL! DrehbezX HorzFL! PinY, HorzFL! Winkel) 
  
Gibt die *y* -Koordinate für den Schnittpunkt von VertFL und HorzFL in Seiteneinheiten. 
  

