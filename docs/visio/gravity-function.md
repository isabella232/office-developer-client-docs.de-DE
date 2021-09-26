---
title: GRAVITY-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251433
ms.localizationpriority: medium
ms.assetid: db80f147-71a0-0b23-bc7e-fe1915dfdd21
description: Berechnet den richtigen Drehwinkel eines Textblocks für die angegebene Formdrehung, um zu verhindern, dass der Text auf den Kopf gestellt wird.
ms.openlocfilehash: f8a564160fae9fe85b531631215de536a8c28406
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612711"
---
# <a name="gravity-function"></a>GRAVITY Function

Berechnet den richtigen Drehwinkel eines Textblocks für die angegebene Formdrehung, um zu verhindern, dass der Text auf den Kopf gestellt wird.
  
## <a name="syntax"></a>Syntax

GRAVITY(** *angle* **,[ ** *limit1* ** ],[ ** *limit2* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Winkel_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Winkel des Shapes.  <br/> |
| _Grenzwert1_ <br/> |Optional  <br/> |**String** <br/> |Erste Drehbegrenzung. Der Standardwert beträgt 90 Grad.  <br/> |
| _Limit2_ <br/> |Optional  <br/> |**String** <br/> |Zweite Drehbegrenzung. Der Standardwert beträgt 270 Grad.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Die GRAVITY-Funktion wird gewöhnlich in der Zelle TxtWinkel verwendet. 
  
Der zurückgegebene Wert beträgt 180 Grad, wenn _sich der Winkel_ zwischen den durch _limit1_ und limit2 angegebenen Werten befindet.  andernfalls beträgt der zurückgegebene Wert 0 Grad.
  
Alle Argumente werden von der Funktion automatisch auf einen Wert zwischen 0 und 360 Grad normalisiert. Wenn bei einem Argument keine Einheiten angegeben sind, wird Bogenmaß (Radiant) unterstellt. 
  
## <a name="example-1"></a>Beispiel 1

GRAVITY(Angle)
  
Gibt 180 Grad zurück, wenn  *der Winkel*  zwischen 90 und 270 Grad liegt; andernfalls werden 0 Grad zurückgegeben. 
  
## <a name="example-2"></a>Beispiel 2

GRAVITY(2)
  
Gibt 180 Grad zurück, da 2 Bogenmaße (Radiant) zwischen 90 und 270 Grad liegen.
  
## <a name="example-3"></a>Beispiel 3

GRAVITY(100 deg, 110 deg, 290 deg)
  
Gibt 0 Grad zurück.
  
## <a name="example-4"></a>Beispiel 4

GRAVITY(100 deg, 290 deg, 110 deg)
  
Gibt 0 Grad zurück.
  

