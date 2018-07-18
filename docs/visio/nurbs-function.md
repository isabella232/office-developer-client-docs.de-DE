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
description: Gibt ein nonuniform rationales B-Spline (NURBS). Diese Funktion wird in der Zelle E NURBS verwendet.
ms.openlocfilehash: 005a66b9da2425beaf416ec2273c10446c183add
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19797588"
---
# <a name="nurbs-function"></a>NURBS Function

Gibt ein nonuniform rationales B-Spline (NURBS). Diese Funktion wird in der Zelle E NURBS verwendet.
  
## <a name="syntax"></a>Syntax

NURBS (** *KnotZuletst* **, ** *Grad* **, ** *xTyp gleich* **, ** *gleich* **, ** *X1* **, ** *y1* **, ** *knot1* **, ** *Gewicht1* **,...) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _KnotZuletst_ <br/> |Erforderlich  <br/> |**string** <br/> | Der letzte Knoten.  <br/> |
| _Grad_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Gradwert des Splines.  <br/> |
| _xTyp gleich_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Gibt an, wie die _X_ -Eingabedaten interpretiert werden. Wenn _xTyp gleich_ 0 ist, werden alle _x_ eingegebenen Daten als Prozentsatz der Breite interpretiert. Wenn _xTyp gleich_ 1 ist, werden alle _X_ Eingabedaten als lokale Koordinaten interpretiert.  <br/> |
| _Gleich_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Gibt an, wie die _y_ -Eingabedaten interpretiert werden. Wenn _gleich_ 0 ist, werden alle eingegebenen _y_ -Daten als Prozentsatz der Höhe interpretiert. Wenn _gleich_ 1 ist, werden alle _y_ eingegebenen Daten als lokale Koordinaten interpretiert.  <br/> |
| _x1_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine x-Koordinate.  <br/> |
| _Y1_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine y-Koordinate.  <br/> |
| _Knot1_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Knoten auf dem B-Spline.  <br/> |
| _Gewicht1_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine Breite für das B-Spline.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Für jedes *X* -Argument muss ein *y* -Argument; Andernfalls wird ein Fehler zurückgegeben. 
  
Sie müssen mindestens eine *X*, *y*, *Knoten* und *Weight* -Argument angeben. andernfalls, gibt Visio einen Fehler zurück. 
  

