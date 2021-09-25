---
title: ANG360-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
ms.localizationpriority: medium
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: Normalisiert den Bereich eines Winkels.
ms.openlocfilehash: b94af0ea3d20c839f9bb314e042b2c19da0f0820
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603942"
---
# <a name="ang360-function"></a>ANG360 Function

Normalisiert den Bereich eines Winkels auf 0 \< = Ergebnis \< 2PI Bogenmaß (0 \< = Ergebnis \< 360 Grad).
  
## <a name="syntax"></a>Syntax

ANG360(***angle*** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Winkel_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der zu normalisierende Winkel.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn  *der Winkel*  nicht mithilfe von Winkeleinheiten angegeben wird, wird er als Bogenmaß interpretiert. Wenn  *winkel*  nicht in einen Wert konvertiert werden kann, ein #VALUE! zurückgegeben. 
  
## <a name="example-1"></a>Beispiel 1

ANG360(395 deg)
  
Gibt 35 deg zurück.
  
## <a name="example-2"></a>Beispiel 2

ANG360(-9,8 rad.)
  
Gibt 2,7664 Rad zurück.
  
## <a name="example-3"></a>Beispiel 3

ANG360(45)
  
Gibt 58,31 deg (1,0177 Rad) zurück.
  

