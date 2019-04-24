---
title: ASIN-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
localization_priority: Normal
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Gibt den arcsine einer Zahl zurück, beispielsweise den Winkel, dessen Sinus Nummer ist.
ms.openlocfilehash: a7585dc07053466203f11cc04ce249ceb62fbda0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341524"
---
# <a name="asin-function"></a>ASIN Function

Gibt den arcsine einer Zahl zurück, beispielsweise den Winkel, dessen Sinus *Nummer* ist. 
  
## <a name="syntax"></a>Syntax

Arcs (* * *Number* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Der Sinus des Winkels.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Eingabewert muss im Range-1 < = *Number* < = 1 oder ein #NUM! zurückgegeben. Der resultierende Winkel befindet sich im Range-PI/2 < ** = Angle _LT_ = Pi/2 Radiant (-90 < = *winkel* < = 90 Grad). 
  
## <a name="example"></a>Beispiel

ARCS (1)
  
Gibt 90 deg zurück.
  

