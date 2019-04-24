---
title: ANG360-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
localization_priority: Normal
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: Normalisiert den Range eines Winkels.
ms.openlocfilehash: 017dd89bd3b814c10422cd32eea1ee7e343eaf50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341489"
---
# <a name="ang360-function"></a>ANG360 Function

Normalisiert den \<Range eines Winkels auf 0 = Ergebnis \< 2pi Bogenmaß (0 \<= Ergebnis \< 360 Grad).
  
## <a name="syntax"></a>Syntax

ANG360 (* * *Winkel* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Winkel_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Der zu normalisierende Winkel.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn *Angle* nicht mithilfe von Winkeleinheiten angegeben wird, wird er als Bogenmaß interpretiert. Wenn *Angle* nicht in einen Wert konvertiert werden kann, wird ein #VALUE! zurückgegeben. 
  
## <a name="example-1"></a>Beispiel 1

ANG360(395 deg)
  
Gibt 35 deg zurück.
  
## <a name="example-2"></a>Beispiel 2

ANG360(-9,8 rad.)
  
Gibt 2,7664 Rad zurück.
  
## <a name="example-3"></a>Beispiel 3

ANG360 (45)
  
Gibt 58,31 deg (1,0177 Rad) zurück.
  

