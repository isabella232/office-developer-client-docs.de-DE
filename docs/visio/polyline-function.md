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
description: Gibt eine Polylinie zurück. Diese Funktion wird in der Zelle PolyLineTo Geometriezeilen verwendet.
ms.openlocfilehash: afe31b3963cca03d0273b8768f6cc5538d1850ee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797635"
---
# <a name="polyline-function"></a>POLYLINE Function

Gibt eine Polylinie zurück. Diese Funktion wird in der Zelle PolyLineTo Geometriezeilen verwendet. 
  
## <a name="syntax"></a>Syntax

POLYLINIE (** *xTyp gleich* **, ** *gleich* **, ** *X1* **, ** *y1* **...) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _xTyp gleich_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Gibt an, wie die _X_ -Eingabedaten interpretiert werden. Ist _xTyp gleich_ 0, werden die eingegebenen _X_-Daten als Prozentsatz der Breite interpretiert werden. Ist _xTyp gleich_ 1, werden die eingegebenen _X_-Daten als eine lokale Koordinate interpretiert werden.  <br/> |
| _Gleich_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Gibt an, wie Interpretieren der _y_-Eingabedaten. Ist _gleich_ 0, werden die eingegebenen _y_-Daten als Prozentsatz der Höhe interpretiert werden. Ist _gleich_ 1, werden die eingegebenen _y_-Daten als eine lokale Koordinate interpretiert werden.  <br/> |
| _x1_ <br/> |Erforderlich  <br/> |**Nummer** <br/> | Eine _X_-Koordinate.  <br/> |
| _Y1_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Eine _y_-Koordinate.  <br/> |
   
## <a name="remarks"></a>Hinweise

Für jedes *X* -Argument muss ein *y* -Argument; Andernfalls wird ein Fehler zurückgegeben. 
  
## <a name="example"></a>Beispiel

POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0) 
  
Gibt ein Rechteck der Dimensionen Breite x Höhe zurück. 
  

