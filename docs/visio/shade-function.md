---
title: SHADE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Ändert die Farbe, indem die Leuchtdichte um den im int-Parameter angegebenen Wert (positiv oder negativ) verringert wird.
ms.openlocfilehash: 1e9c967cb72a838f4792d3ac47fa61da54dd424a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570092"
---
# <a name="shade-function"></a>SHADE Function

Ändert die Farbe, indem die Leuchtdichte um den im  _int-Parameter_ angegebenen Wert (positiv oder negativ) verringert wird. 
  
## <a name="syntax"></a>Syntax

SHADE(** *color* **, ** *int* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Farbindex von Microsoft Visio oder der RGB-Wert der Farbe.  <br/> |
| _int_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der Wert, um den die Leuchtdichte der Farbe verringert werden soll. Kann positiv oder negativ sein.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **RGB**
  
## <a name="remarks"></a>HinwBemerkungeneise

Die unteren und oberen Grenzwerte der Leuchtdichte liegen jeweils bei 0 und 240. Es gibt keine Beschränkung für die Größe der ganzen Zahl, die Sie für den  _int-Parameter_ übergeben können, aber die Leuchtdichte überschreitet diese Grenzwerte nie. 
  
![Obere und untere Grenzwerte der Leuchtdichte](media/image199_ZA10173627.gif)
  

