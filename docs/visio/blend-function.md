---
title: BLEND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Mischt zwei Farben in dem durch den float-Parameter angegebenen Verhältnis.
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432786"
---
# <a name="blend-function"></a>BLEND Function

Mischt zwei Farben in dem durch den  _float-Parameter angegebenen_ Verhältnis. 
  
## <a name="syntax"></a>Syntax

BLEND(** *color1* **, ** *color2* **, ** *float[0,1]* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _color1_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Farbindex von Visio oder der RGB-Wert der ersten Farbe.  <br/> |
| _color2_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Farbindex von Visio oder der RGB-Wert der zweiten Farbe.  <br/> |
| _float[0,1]_ <br/> |Erforderlich  <br/> |**Float** <br/> |Das Verhältnis, in dem  _Farbe2_ bzw.  _Farbe1_ gemischt werden soll. Eine reelle Zahl zwischen 0 und 1.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **RGB**
  
## <a name="remarks"></a>Hinweise

Die zurückgegebene Farbe wird durch die relativen Proportionen bestimmt, in denen  _color2_ und  _color1_ bzw. , wie durch den  _float-Parameter angegeben, gemischt_ werden. Wenn float  _z._ B. 0,25 ist, besteht die zurückgegebene Farbe aus 75 % von  _Color1_ und 25 %  _von Color2_. 
  
Eine weitere Möglichkeit, sich darüber Gedanken zu machen, ist, dass der _Float-Wert_ dem Punkt entlang des Farbspektrums von _Color1_ bis _Color2 entspricht._ Daher werden kleinere Zahlen (näher  an Null) für float näher an _Farbe1_ erzeugt, während größere Zahlen (näher an 1) Blends näher an _Color2 erzeugen._
  

