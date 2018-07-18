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
description: Gibt den Arkussinus einer Zahl, beispielsweise der Winkel, dessen Sinus Zahl ist.
ms.openlocfilehash: e5ed8f9fc8c85ac4816fede03bfe6f6af5cbf5f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796431"
---
# <a name="asin-function"></a>ASIN Function

Gibt den Arkussinus einer Zahl, beispielsweise der Winkel, dessen Sinus *Zahl* ist. 
  
## <a name="syntax"></a>Syntax

ASIN (** *Anzahl* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Sinus des Winkels.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert muss im Bereich von-1 < = *Zahl* < = 1 oder ein #NUM! Fehler wird zurückgegeben. Der resultierende Winkel liegt im Bereich-PI/2 < = *Winkel* < = PI/2 Bogenmaß (-90 < = *Winkel* < = 90 Grad). 
  
## <a name="example"></a>Beispiel

ASIN(1)
  
Gibt 90 deg zurück.
  

