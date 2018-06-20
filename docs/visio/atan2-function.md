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
description: Gibt den Winkel zwischen dem Vektor X, y und die Richtung der X-Achse. Das Ergebnis ist eine Zahl in der aktuellen Maßeinheit für Winkel.
ms.openlocfilehash: dfd62ce628a3a46ff14b3ffc3f07074a39c66e14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796395"
---
# <a name="atan2-function"></a>ATAN2 Function

Gibt den Winkel zwischen dem Vektor *X, y* und die Richtung der *X* -Achse. Das Ergebnis ist eine Zahl in der aktuellen Maßeinheit für Winkel. 
  
## <a name="syntax"></a>Syntax

ATAN2 (** *y* **, ** *X* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _y_ <br/> |Erforderlich  <br/> |**Numerische** <br/> |Die _y_-Wert des Punkts.  <br/> |
| _x_ <br/> |Erforderlich  <br/> |**Numerische** <br/> |Die _X_-Wert des Punkts.  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Arkustangens ist der Winkel gegen den Uhrzeigersinn gemessen, aus der positiven *X* -Achse zu einer Zeile, die den Ursprung (0,0) und den durch die *x-* und *y* dargestellten Punkt überschneidet. In Microsoft Visio gibt ATAN2(0,0) den Wert 0 zurück. Um das Ergebnis von ATAN2 in einem anderen Winkelmaß zu erzwingen, verwenden Sie die Funktionen DEG oder RAD. 
  
ATAN2-Funktion ist die Gegenfunktion von TAN-Funktion. Die ATAN2-Funktion gibt den Winkel, dessen Tangens gleich *y* geteilt durch *x* ist. Wenn ATAN2 (*y, X*) stellt einen Winkel in ein rechtwinkliges Dreieck und *y* ist die "gegenüberliegenden Seite" *X* ist der "angrenzenden Seite", damit die Funktion auch als ATAN2(Gegenkathete,Ankathete) geschrieben werden könnte. 
  
## <a name="example-1"></a>Beispiel 1

ATAN2(1.25,2.25)
  
Gibt 29,0456 deg zurück.
  
## <a name="example-2"></a>Beispiel 2

ATAN2(1,WURZEL(3))
  
Gibt 30 deg zurück.
  
## <a name="example-3"></a>Beispiel 3

ATAN2(1,1)
  
Gibt 45 deg zurück.
  

