---
title: ATAN2-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251397
ms.localizationpriority: medium
ms.assetid: 524278fb-196e-9cf9-e27b-d03642beeee4
description: Gibt den Winkel zwischen dem Vektor zurück, der durch x,y dargestellt wird, und der Richtung der x-Achse. Das Resultat ist eine Zahl in der aktuellen Maßeinheit für Winkel.
ms.openlocfilehash: faa4e450483e920d0ffc7b40e17a48018dfc4d87
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598822"
---
# <a name="atan2-function"></a>ATAN2 Function

Gibt den Winkel zwischen dem Vektor zurück, der durch *x,y* dargestellt wird, und der Richtung der *x-Achse.* Das Resultat ist eine Zahl in der aktuellen Maßeinheit für Winkel. 
  
## <a name="syntax"></a>Syntax

ATAN2(** *y* **, ** *x* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _y_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der  _y-Wert_ des Punkts.  <br/> |
| _x_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der  _x-Wert_ des Punkts.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Arctangent ist der Winkel, der gegen den Uhrzeigersinn von der positiven  *x-Achse*  zu einer Linie gemessen wird, die den Ursprung (0,0) und den durch  *x*  und  *y*  dargestellten Punkt überschneidet. In Microsoft Visio gibt ATAN2(0,0) 0 zurück. Verwenden Sie die DEG- oder RAD-Funktion, um das Ergebnis von ATAN2 in eine andere Winkelmessung zu erzwingen. 
  
Die ATAN2-Funktion ist die Antifunktion der TAN-Funktion. Die ATAN2-Funktion gibt den Winkel zurück, dessen Winkel gleich *y* ist, dividiert durch *x.* Wenn ATAN2(*y,x*) einen Winkel in einem rechtwinkligen Dreieck darstellt, ist  *y*  die "gegenüberliegende Seite" und  *x*  die "benachbarte Seite", sodass die Funktion als ATAN2(gegenüber, nebeneinander) geschrieben werden kann. 
  
## <a name="example-1"></a>Beispiel 1

ATAN2(1.25,2.25)
  
Gibt 29,0456 deg zurück.
  
## <a name="example-2"></a>Beispiel 2

ATAN2(1,SQRT(3))
  
Gibt 30 deg zurück.
  
## <a name="example-3"></a>Beispiel 3

ATAN2(1,1)
  
Gibt 45 deg zurück.
  

