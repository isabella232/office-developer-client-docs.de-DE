---
title: ATAN2-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251397
localization_priority: Normal
ms.assetid: 524278fb-196e-9cf9-e27b-d03642beeee4
description: Gibt den Winkel zwischen dem durch x,y dargestellten Vektor und der Richtung der x-Achse zurück. Das Resultat ist eine Zahl in der aktuellen Maßeinheit für Winkel.
ms.openlocfilehash: 906c024f2a78d6e11c1bbf770c14d04299cadca8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436482"
---
# <a name="atan2-function"></a>ATAN2 Function

Gibt den Winkel zwischen dem durch  *x,y*  dargestellten Vektor und der Richtung der  *x-Achse*  zurück. Das Resultat ist eine Zahl in der aktuellen Maßeinheit für Winkel. 
  
## <a name="syntax"></a>Syntax

ATAN2(** *y* **, ** *x* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _y_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der  _y-Wert_ des Punkts.  <br/> |
| _x_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der  _x-Wert_ des Punkts.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das arctangent ist der Winkel, der gegen den Uhrzeigersinn von der positiven *x-Achse* zu einer Linie gemessen wird, die den Ursprung (0,0) und den durch *x* und y dargestellten Punkt *überschneidet.* Atan2(0,0) gibt in Microsoft Visio 0 zurück. Verwenden Sie die DEG- oder RAD-Funktion, um das Ergebnis von ATAN2 in eine andere Winkelmessung zu erzwingen. 
  
Die ATAN2-Funktion ist die Antifunktion der TAN-Funktion. Die ATAN2-Funktion gibt den Winkel zurück, dessen Winkel *y* dividiert durch *x ist.* Wenn ATAN2(*y,x*) einen Winkel in einem rechten Dreieck darstellt,  *ist y*  die "gegenüberliegende Seite" und  *x*  die "angrenzende Seite", sodass die Funktion als ATAN2(gegenüber, nebenan) geschrieben werden kann. 
  
## <a name="example-1"></a>Beispiel 1

ATAN2(1.25,2.25)
  
Gibt 29,0456 deg zurück.
  
## <a name="example-2"></a>Beispiel 2

ATAN2(1,SQRT(3))
  
Gibt 30 deg zurück.
  
## <a name="example-3"></a>Beispiel 3

ATAN2(1,1)
  
Gibt 45 deg zurück.
  

