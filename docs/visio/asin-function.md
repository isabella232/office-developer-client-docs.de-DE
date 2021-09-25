---
title: ASIN-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
ms.localizationpriority: medium
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Gibt den Arkussinus einer Zahl zurück, z. B. den Winkel, dessen Sinus zahl ist.
ms.openlocfilehash: d3cc3bb4afcb537f0234d4a5e51fc3fee00d809d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628864"
---
# <a name="asin-function"></a>ASIN Function

Gibt den Arkussinus einer Zahl zurück, z. B. den Winkel, dessen Sinus  *zahl*  ist. 
  
## <a name="syntax"></a>Syntax

ASIN(***number*** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Sinus des Winkels.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Eingabewert muss im Bereich -1 <=  *Zahl*  <= 1 oder ein #NUM! zurückgegeben. Der resultierende Winkel liegt im Bereich -PI/2 <=  *Winkel*  <= PI/2 Bogenmaß (-90 <=  *Winkel*  <= 90 Grad). 
  
## <a name="example"></a>Beispiel

ASIN(1)
  
Gibt 90 deg zurück.
  

