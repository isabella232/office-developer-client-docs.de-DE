---
title: TINT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Ändert die Farbe, indem ihre Leuchtkraft um den im int-Parameter angegebenen Wert (positiv oder negativ) erhöht wird.
ms.openlocfilehash: 8924bc0662814e14d01b4bd5332f5fadeb0a1082
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406577"
---
# <a name="tint-function"></a>TINT-Funktion

Ändert die Farbe, indem ihre Leuchtkraft um den im  _int-Parameter_ angegebenen Wert (positiv oder negativ) erhöht wird. 
  
## <a name="syntax"></a>Syntax

TINT(** *color* **, ** *int* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Farbindex von Microsoft Visio oder der RGB-Wert der Farbe.  <br/> |
| _int_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der Wert, um den die Leuchtdichte der Farbe erhöht werden soll. Kann positiv oder negativ sein.
  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **RGB**
  
## <a name="remarks"></a>Hinweise

Die unteren und oberen Grenzwerte der Leuchtdichte liegen jeweils bei 0 und 240. Es gibt keine Beschränkung für die Größe der ganzen Zahl, die Sie für den  _int-Parameter_ übergeben können, aber die Leuchtkraft überschreitet diese Grenzwerte nie. 
  

