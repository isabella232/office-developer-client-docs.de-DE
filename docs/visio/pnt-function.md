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
description: Gibt den durch die Koordinaten x und y dargestellten Punkt als Single-Wert zurück.
ms.openlocfilehash: c0a12aa18f4c766ea1f5b0fa1d827804d766713c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322351"
---
# <a name="pnt-function"></a>PNT Function

Gibt den durch die Koordinaten _x_ und _y_ dargestellten Punkt als Single-Wert zurück. 
  
## <a name="syntax"></a>Syntax

PNT (* * *x, y* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _x, y_ <br/> |Erforderlich  <br/> |**Number, Number** <br/> |Die Koordinaten des Punkts im Koordinatensystem des aktuellen Shapes.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeigen
  
## <a name="remarks"></a>Bemerkungen

Durch das Konvertieren von Koordinaten in Punkt können Sie die Geometrie eines Shapes ändern, ohne *x* -und *y* -Koordinaten separat bearbeiten zu müssen. 
  
## <a name="example"></a>Beispiel

PNT (PinX, PinY) 
  
Gibt den durch DrehbezX und DrehbezY dargestellten Punkt zurück. 
  

