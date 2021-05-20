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
description: Gibt den Punkt zurück, der durch die Koordinaten x und y als einzelner Wert dargestellt wird.
ms.openlocfilehash: c0a12aa18f4c766ea1f5b0fa1d827804d766713c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435712"
---
# <a name="pnt-function"></a>PNT Function

Gibt den Punkt zurück, der durch die Koordinaten  _x_ und  _y_ als einzelner Wert dargestellt wird. 
  
## <a name="syntax"></a>Syntax

PNT(** *x,y* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _x,y_ <br/> |Erforderlich  <br/> |**Number, Number** <br/> |Die Koordinaten des Punkts im Koordinatensystem des aktuellen Shapes.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeigen
  
## <a name="remarks"></a>Hinweise

Wenn Sie Koordinaten in Punkt konvertieren, können Sie die Geometrie eines Shapes ändern, ohne  *X-*  und  *Y-Koordinaten*  separat bearbeiten zu müssen. 
  
## <a name="example"></a>Beispiel

PNT(PinX,PinY) 
  
Gibt den durch DrehbezX und DrehbezY dargestellten Punkt zurück. 
  

