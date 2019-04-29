---
title: ANGLETOPAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253218
localization_priority: Normal
ms.assetid: 4d87313a-c09a-582c-04f4-d95800e3e9f2
description: Gibt einen transformierten Winkel im übergeordneten Koordinatensystem des Ziel-Shapes zurück. Konvertiert einen Winkel aus lokalen Koordinaten in einem Quell-Shape in die übergeordneten Koordinaten eines Ziel-Shapes.
ms.openlocfilehash: e411cbae21d832039e2fbda93393a8fe0bd1f9f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404323"
---
# <a name="angletopar-function"></a>ANGLETOPAR Function

Gibt einen transformierten Winkel im übergeordneten Koordinatensystem des Ziel-Shapes zurück. Konvertiert einen Winkel aus lokalen Koordinaten in einem Quell-Shape in die übergeordneten Koordinaten eines Ziel-Shapes. 
  
## <a name="syntax"></a>Syntax

ANGLETOPAR (* * *srcAngle* * *, * * *srcRef* * *, * * *Zielbezug* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _srcAngle_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Ein Winkel im Quellkoordinatensystem.  <br/> |
| _srcRef_ <br/> |Erforderlich  <br/> |**String** <br/> | Ein Bezug auf eine Zelle im Quellobjekt, beispielsweise ein Shape, eine Gruppe, ein Zeichenblatt usw.  <br/> |
| _Zielbezug_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Bezug auf eine Zelle im Zielobjekt, beispielsweise ein Shape, eine Gruppe, ein Zeichenblatt usw.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Funktion ist auch dann ausführbar, wenn die Ausgangs- und Ziel-Shapes in Gruppen eingebunden sind. Wird ebenfalls für Dreh- und Kippvorgänge in der Zwischentransformation angepasst.
  
Die Ausgangs- und Zielkoordinaten müssen auf dem gleichen Zeichenblatt sein.
  
Wenn das Ziel ein Zeichenblatt ohne übergeordnetes Objekt ist, wird das Ergebnis in den lokalen Koordinaten des Zeichenblatts ausgedrückt.
  

