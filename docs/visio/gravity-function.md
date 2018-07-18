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
description: Berechnet einen Textblock richtigen Winkel der Drehung für die Drehung der angegebenen Form um zu verhindern, dass den Text auf dem Kopf steht.
ms.openlocfilehash: 0d8b0160c7e7d63fb5a272219a2694d35e6e6b61
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19797110"
---
# <a name="gravity-function"></a>GRAVITY Function

Berechnet einen Textblock richtigen Winkel der Drehung für die Drehung der angegebenen Form um zu verhindern, dass den Text auf dem Kopf steht.
  
## <a name="syntax"></a>Syntax

GRAVITY (** *Winkel* **, [** *Grenze1* **], [** *Grenze2* **]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Winkel_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Winkel des Shapes.  <br/> |
| _Grenze1_ <br/> |Optional  <br/> |**String** <br/> |Erste Drehbegrenzung. Der Standardwert beträgt 90 Grad.  <br/> |
| _Grenze2_ <br/> |Optional  <br/> |**String** <br/> |Zweite Drehbegrenzung. Der Standardwert beträgt 270 Grad.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Die GRAVITY-Funktion wird gewöhnlich in der Zelle TxtWinkel verwendet. 
  
Der zurückgegebene Wert ist 180 Grad, wenn der _Winkel_ zwischen den _Grenze1_ und _Grenze2_angegebenen Werten liegt. Andernfalls ist der zurückgegebene Wert 0 Grad.
  
Alle Argumente werden von der Funktion automatisch auf einen Wert zwischen 0 und 360 Grad normalisiert. Wenn bei einem Argument keine Einheiten angegeben sind, wird Bogenmaß (Radiant) unterstellt. 
  
## <a name="example-1"></a>Beispiel 1

GRAVITY(Winkel)
  
Gibt 180 Grad, wenn der *Winkel* zwischen 90 und 270 Grad liegt; andernfalls gibt 0 Grad zurück. 
  
## <a name="example-2"></a>Beispiel 2

GRAVITY(2)
  
Gibt 180 Grad zurück, da 2 Bogenmaße (Radiant) zwischen 90 und 270 Grad liegen.
  
## <a name="example-3"></a>Beispiel 3

GRAVITY(100 deg, 110 deg, 290 deg)
  
Gibt 0 Grad zurück.
  
## <a name="example-4"></a>Beispiel 4

GRAVITY(100 deg, 290 deg, 110 deg)
  
Gibt 0 Grad zurück.
  

