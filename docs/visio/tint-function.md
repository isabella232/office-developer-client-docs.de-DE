---
title: TINT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Ändert die Farbe, indem die Helligkeit um die im Parameter int angegebene Menge (positiv oder negativ) erhöht wird.
ms.openlocfilehash: 8924bc0662814e14d01b4bd5332f5fadeb0a1082
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280931"
---
# <a name="tint-function"></a>TINT-Funktion

Ändert die Farbe, indem die Helligkeit um die im Parameter _int_ angegebene Menge (positiv oder negativ) erhöht wird. 
  
## <a name="syntax"></a>Syntax

Farbton (* * *Farbe* * *, * * *int* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Der Farbindex von Microsoft Visio oder der RGB-Wert der Farbe.  <br/> |
| _int_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der Wert, um den die Leuchtdichte der Farbe erhöht werden soll. Kann positiv oder negativ sein.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **RGB**
  
## <a name="remarks"></a>Bemerkungen

Die unteren und oberen Grenzwerte der Leuchtdichte liegen jeweils bei 0 und 240. Es gibt keine Begrenzung für die Größe der Ganzzahl, die Sie für den _int_ -Parameter übergeben können, aber die Luminanz überschreitet diese Grenzwerte nie. 
  

