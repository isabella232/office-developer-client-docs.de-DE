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
description: Gibt den Winkel zwischen dem durch x, y und der Richtung der x-Achse dargestellten Vektor zurück. Das Resultat ist eine Zahl in der aktuellen Maßeinheit für Winkel.
ms.openlocfilehash: 906c024f2a78d6e11c1bbf770c14d04299cadca8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436482"
---
# <a name="atan2-function"></a>ATAN2 Function

Gibt den Winkel zwischen dem durch *x, y* und der Richtung der *x* -Achse dargestellten Vektor zurück. Das Resultat ist eine Zahl in der aktuellen Maßeinheit für Winkel. 
  
## <a name="syntax"></a>Syntax

ATAN2 (* * *y* * *, * * *x* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _y_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der _y_-Wert des Punkts.  <br/> |
| _x_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der _x_-Wert des Punkts.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Arctangent ist der Winkel, der von der positiven *x* -Achse gegen den Uhrzeigersinn gemessen wird, zu einer Linie, die den Ursprung (0,0) und den durch *x* und *y* dargestellten Punkt schneidet. In Microsoft Visio gibt ATAN2 (0, 0) 0 zurück. Wenn Sie das Ergebnis von ATAN2 in eine andere Winkelmessung erzwingen möchten, verwenden Sie die DEG-oder die RAD-Funktion. 
  
Die ATAN2-Funktion ist die antifunktion der TAN-Funktion. Die ATAN2-Funktion gibt den Winkel zurück, dessen Winkel gleich *y* geteilt durch *x* ist. Wenn ATAN2 (*y, x*) einen Winkel in einem rechtwinkligen Dreieck darstellt, ist *y* die "Gegenseite" und *x* die benachbarte Seite, sodass die Funktion als atan2 (gegenüber, benachbart) geschrieben werden kann. 
  
## <a name="example-1"></a>Beispiel 1

ATAN2 (1.25, 2.25)
  
Gibt 29,0456 deg zurück.
  
## <a name="example-2"></a>Beispiel 2

ATAN2 (1, SQRT (3))
  
Gibt 30 deg zurück.
  
## <a name="example-3"></a>Beispiel 3

ATAN2 (1, 1)
  
Gibt 45 deg zurück.
  

