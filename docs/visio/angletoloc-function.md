---
title: ANGLETOLOC-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253217
localization_priority: Normal
ms.assetid: ee5e3898-bb49-57c6-0ebe-12e1fe388e55
description: Gibt einen transformierten Winkel im lokalen Koordinatensystem des Ziel-Shapes zurück. Konvertiert einen Winkel aus lokalen Koordinaten in einem Quell-Shape in die lokalen Koordinaten eines Ziel-Shapes.
ms.openlocfilehash: 804faeb24932e414ad03bc9e8487c62ca08bd7d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341475"
---
# <a name="angletoloc-function"></a>ANGLETOLOC Function

Gibt einen transformierten Winkel im lokalen Koordinatensystem des Ziel-Shapes zurück. Konvertiert einen Winkel aus lokalen Koordinaten in einem Quell-Shape in die lokalen Koordinaten eines Ziel-Shapes. 
  
## <a name="syntax"></a>Syntax

ANGLETOLOC (* * *srcAngle* * *, * * *srcRef* * *, * * *Zielbezug* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _srcAngle_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Ein Winkel im Quellkoordinatensystem.  <br/> |
| _srcRef_ <br/> |Erforderlich  <br/> |**String** <br/> | Ein Bezug auf eine Zelle im Quellobjekt, beispielsweise ein Shape, eine Gruppe, ein Zeichenblatt usw.  <br/> |
| _Zielbezug_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Bezug auf eine Zelle im Zielobjekt, beispielsweise ein Shape, eine Gruppe, ein Zeichenblatt usw.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Mithilfe der ANGLETOLOC-Funktion können Sie lokale Winkelzellen in einem Shape in Form eines Winkels aus einer anderen Koordinatenstelle festlegen.
  
Diese Funktion ist auch dann ausführbar, wenn die Ausgangs- und Ziel-Shapes in Gruppen eingebunden sind. Wird ebenfalls für Dreh- und Kippvorgänge in der Zwischentransformation angepasst.
  
Die Ausgangs- und Zielkoordinaten müssen auf dem gleichen Zeichenblatt liegen.
  

