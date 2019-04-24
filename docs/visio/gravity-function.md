---
title: GRAVITY-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251433
localization_priority: Normal
ms.assetid: db80f147-71a0-0b23-bc7e-fe1915dfdd21
description: Berechnet den korrekten Drehwinkel des Textblocks für die angegebene Form Drehung, um zu verhindern, dass der Text auf den Kopf gestellt wird.
ms.openlocfilehash: 77c944d954292e231f8bacbe3c8a4433aad5d689
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360186"
---
# <a name="gravity-function"></a>GRAVITY Function

Berechnet den korrekten Drehwinkel des Textblocks für die angegebene Form Drehung, um zu verhindern, dass der Text auf den Kopf gestellt wird.
  
## <a name="syntax"></a>Syntax

Gravitation (* * *Angle* * *, [* * *beschränkung1* * *], [* * *limit2* * *]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Winkel_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Winkel des Shapes.  <br/> |
| _beschränkung1_ <br/> |Optional  <br/> |**String** <br/> |Erste Drehbegrenzung. Der Standardwert beträgt 90 Grad.  <br/> |
| _limit2_ <br/> |Optional  <br/> |**String** <br/> |Zweite Drehbegrenzung. Der Standardwert beträgt 270 Grad.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Die GRAVITY-Funktion wird gewöhnlich in der Zelle TxtWinkel verwendet. 
  
Der zurückgegebene Wert ist __ 180 Grad, wenn Angle zwischen den durch _beschränkung1_ und _limit2_angegebenen Werten liegt. Andernfalls ist der zurückgegebene Wert 0 Grad.
  
Alle Argumente werden von der Funktion automatisch auf einen Wert zwischen 0 und 360 Grad normalisiert. Wenn bei einem Argument keine Einheiten angegeben sind, wird Bogenmaß (Radiant) unterstellt. 
  
## <a name="example-1"></a>Beispiel 1

GRAVITATION (Winkel)
  
Gibt 180 Grad zurück ** , wenn Angle zwischen 90 und 270 Grad liegt; Andernfalls gibt 0 Grad zurück. 
  
## <a name="example-2"></a>Beispiel 2

GRAVITATION (2)
  
Gibt 180 Grad zurück, da 2 Bogenmaße (Radiant) zwischen 90 und 270 Grad liegen.
  
## <a name="example-3"></a>Beispiel 3

GRAVITY(100 deg, 110 deg, 290 deg)
  
Gibt 0 Grad zurück.
  
## <a name="example-4"></a>Beispiel 4

GRAVITY(100 deg, 290 deg, 110 deg)
  
Gibt 0 Grad zurück.
  

