---
title: PNT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251480
ms.localizationpriority: medium
ms.assetid: d14a735c-0278-922f-7823-79adf6cb1e64
description: Gibt den durch die Koordinaten x und y dargestellten Punkt als einen einzelnen Wert zurück.
ms.openlocfilehash: b6c0c9b15aa6b6fb640d433dd866e1977191f872
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573747"
---
# <a name="pnt-function"></a>PNT Function

Gibt den durch die Koordinaten  _x_ und  _y_ dargestellten Punkt als einen einzelnen Wert zurück. 
  
## <a name="syntax"></a>Syntax

PNT(** *x,y* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _x, y_ <br/> |Erforderlich  <br/> |**Number, Number** <br/> |Die Koordinaten des Punkts im Koordinatensystem des aktuellen Shapes.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeigen
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie Koordinaten in Punkte konvertieren, können Sie die Geometrie eines Shapes ändern, ohne die  *X-*  und  *Y-Koordinaten*  separat bearbeiten zu müssen. 
  
## <a name="example"></a>Beispiel

PNT(PinX, PinY) 
  
Gibt den durch DrehbezX und DrehbezY dargestellten Punkt zurück. 
  

