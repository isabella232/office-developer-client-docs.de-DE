---
title: PNT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251480
localization_priority: Normal
ms.assetid: d14a735c-0278-922f-7823-79adf6cb1e64
description: Gibt den Punkt, dargestellt durch die Koordinaten X und y als einen single-Wert.
ms.openlocfilehash: be00f7d5ae55f70407e35eca43881a6d3f70ec13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797688"
---
# <a name="pnt-function"></a>PNT Function

Gibt den durch die Koordinaten _X_ und _y_ als einzelner Wert dargestellten Punkt zurück. 
  
## <a name="syntax"></a>Syntax

PNT (** *x, y* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _X, y_ <br/> |Erforderlich  <br/> |**Number, Number** <br/> |Die Koordinaten des Punkts im Koordinatensystem des aktuellen Shapes.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Punkt
  
## <a name="remarks"></a>Bemerkungen

Konvertierung von Koordinaten in Punkte können Sie die Geometrie eines Shapes ändern, ohne dass zum Bearbeiten von *X* - und *y* -Koordinaten getrennt. 
  
## <a name="example"></a>Beispiel

PNT(PinX,PinY) 
  
Gibt den durch DrehbezX und DrehbezY dargestellten Punkt zurück. 
  

