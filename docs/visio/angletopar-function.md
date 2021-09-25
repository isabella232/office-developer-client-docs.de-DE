---
title: ANGLETOPAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253218
ms.localizationpriority: medium
ms.assetid: 4d87313a-c09a-582c-04f4-d95800e3e9f2
description: Gibt einen transformierten Winkel im übergeordneten Koordinatensystem des Ziel-Shapes zurück. Konvertiert einen Winkel aus lokalen Koordinaten in einem Quell-Shape in die übergeordneten Koordinaten eines Ziel-Shapes.
ms.openlocfilehash: 15be3a0230f439221b1d6a20be63abd456acc4cb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603921"
---
# <a name="angletopar-function"></a>ANGLETOPAR Function

Gibt einen transformierten Winkel im übergeordneten Koordinatensystem des Ziel-Shapes zurück. Konvertiert einen Winkel aus lokalen Koordinaten in einem Quell-Shape in die übergeordneten Koordinaten eines Ziel-Shapes.
    
 
  
## <a name="syntax"></a>Syntax

ANGLETOPAR(***srcAngle** _, _*_srcRef_*_, _ *_dstRef_** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _srcAngle_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Ein Winkel im Quellkoordinatensystem.  <br/> |
| _srcRef_ <br/> |Erforderlich  <br/> |**String** <br/> | Ein Bezug auf eine Zelle im Quellobjekt, beispielsweise ein Shape, eine Gruppe, ein Zeichenblatt usw.  <br/> |
| _dstRef_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Bezug auf eine Zelle im Zielobjekt, beispielsweise ein Shape, eine Gruppe, ein Zeichenblatt usw.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Funktion ist auch dann ausführbar, wenn die Ausgangs- und Ziel-Shapes in Gruppen eingebunden sind. Wird ebenfalls für Dreh- und Kippvorgänge in der Zwischentransformation angepasst.
  
Die Ausgangs- und Zielkoordinaten müssen auf dem gleichen Zeichenblatt sein.
  
Wenn das Ziel ein Zeichenblatt ohne übergeordnetes Objekt ist, wird das Ergebnis in den lokalen Koordinaten des Zeichenblatts ausgedrückt.
  

