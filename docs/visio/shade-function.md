---
title: SHADE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Ändert die Farbe, indem die Helligkeit um die im Parameter int angegebene Menge (positiv oder negativ) verringert wird.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326597"
---
# <a name="shade-function"></a>SHADE Function

Ändert die Farbe, indem die Helligkeit um die im Parameter _int_ angegebene Menge (positiv oder negativ) verringert wird. 
  
## <a name="syntax"></a>Syntax

SCHATTIERUNG (* * *Color* * *, * * *int* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Der Farbindex von Microsoft Visio oder der RGB-Wert der Farbe.  <br/> |
| _int_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der Wert, um den die Leuchtdichte der Farbe verringert werden soll. Kann positiv oder negativ sein.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **RGB**
  
## <a name="remarks"></a>Bemerkungen

Die unteren und oberen Grenzwerte der Leuchtdichte liegen jeweils bei 0 und 240. Es gibt keine Begrenzung für die Größe der Ganzzahl, die Sie für den _int_ -Parameter übergeben können, aber die Luminanz überschreitet diese Grenzwerte nie. 
  
![Ober-und Untergrenze der Helligkeit](media/image199_ZA10173627.gif)
  

