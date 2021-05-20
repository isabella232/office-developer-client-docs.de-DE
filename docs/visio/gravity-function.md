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
description: Berechnet den richtigen Drehwinkel eines Textblocks für die angegebene Formdrehung, um zu verhindern, dass der Text auf den Kopf gestellt wird.
ms.openlocfilehash: 77c944d954292e231f8bacbe3c8a4433aad5d689
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429285"
---
# <a name="gravity-function"></a>GRAVITY Function

Berechnet den richtigen Drehwinkel eines Textblocks für die angegebene Formdrehung, um zu verhindern, dass der Text auf den Kopf gestellt wird.
  
## <a name="syntax"></a>Syntax

GRAVITY(** *angle* **,[ ** *limit1* ** ],[** *limit2* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _angle_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Winkel des Shapes.  <br/> |
| _limit1_ <br/> |Optional  <br/> |**String** <br/> |Erste Drehbegrenzung. Der Standardwert beträgt 90 Grad.  <br/> |
| _limit2_ <br/> |Optional  <br/> |**String** <br/> |Zweite Drehbegrenzung. Der Standardwert beträgt 270 Grad.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Hinweise

Die GRAVITY-Funktion wird gewöhnlich in der Zelle TxtWinkel verwendet. 
  
Der zurückgegebene Wert beträgt 180 Grad, wenn der Winkel zwischen den durch _limit1_ und limit2 angegebenen _Werten liegt._  Andernfalls beträgt der zurückgegebene Wert 0 Grad.
  
Alle Argumente werden von der Funktion automatisch auf einen Wert zwischen 0 und 360 Grad normalisiert. Wenn bei einem Argument keine Einheiten angegeben sind, wird Bogenmaß (Radiant) unterstellt. 
  
## <a name="example-1"></a>Beispiel 1

GRAVITY(Angle)
  
Gibt 180 Grad zurück,  *wenn der Winkel*  zwischen 90 und 270 Grad liegt. Andernfalls werden 0 Grad zurückgegeben. 
  
## <a name="example-2"></a>Beispiel 2

GRAVITY(2)
  
Gibt 180 Grad zurück, da 2 Bogenmaße (Radiant) zwischen 90 und 270 Grad liegen.
  
## <a name="example-3"></a>Beispiel 3

GRAVITY(100 deg, 110 deg, 290 deg)
  
Gibt 0 Grad zurück.
  
## <a name="example-4"></a>Beispiel 4

GRAVITY(100 deg, 290 deg, 110 deg)
  
Gibt 0 Grad zurück.
  

