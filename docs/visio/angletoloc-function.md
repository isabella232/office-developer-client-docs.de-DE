---
title: ANGLETOLOC-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253217
ms.localizationpriority: medium
ms.assetid: ee5e3898-bb49-57c6-0ebe-12e1fe388e55
description: Gibt einen transformierten Winkel im lokalen Koordinatensystem des Ziel-Shapes zurück. Konvertiert einen Winkel aus lokalen Koordinaten in einem Quell-Shape in die lokalen Koordinaten eines Ziel-Shapes.
ms.openlocfilehash: e223c5517b01c881367da19a8cb3c5e3f1c0780b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603928"
---
# <a name="angletoloc-function"></a>ANGLETOLOC Function

Gibt einen transformierten Winkel im lokalen Koordinatensystem des Ziel-Shapes zurück. Konvertiert einen Winkel aus lokalen Koordinaten in einem Quell-Shape in die lokalen Koordinaten eines Ziel-Shapes. 
    
 
  
## <a name="syntax"></a>Syntax

ANGLETOLOC(***srcAngle** _, _*_srcRef_*_, _ *_dstRef_** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _srcAngle_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Ein Winkel im Quellkoordinatensystem.  <br/> |
| _srcRef_ <br/> |Erforderlich  <br/> |**String** <br/> | Ein Bezug auf eine Zelle im Quellobjekt, beispielsweise ein Shape, eine Gruppe, ein Zeichenblatt usw.  <br/> |
| _dstRef_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Bezug auf eine Zelle im Zielobjekt, beispielsweise ein Shape, eine Gruppe, ein Zeichenblatt usw.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Mithilfe der ANGLETOLOC-Funktion können Sie lokale Winkelzellen in einem Shape in Form eines Winkels aus einer anderen Koordinatenstelle festlegen.
  
Diese Funktion ist auch dann ausführbar, wenn die Ausgangs- und Ziel-Shapes in Gruppen eingebunden sind. Wird ebenfalls für Dreh- und Kippvorgänge in der Zwischentransformation angepasst.
  
Die Ausgangs- und Zielkoordinaten müssen auf dem gleichen Zeichenblatt liegen.
  

