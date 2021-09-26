---
title: BLEND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Mischt zwei Farben in dem durch den Float-Parameter angegebenen Verhältnis.
ms.openlocfilehash: bacac9de24fed46f091ea3efaf9801740a918be2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613142"
---
# <a name="blend-function"></a>BLEND Function

Mischt zwei Farben in dem durch den  _Float-Parameter_ angegebenen Verhältnis. 
  
## <a name="syntax"></a>Syntax

BLEND(** *color1* **, ** *color2* **, ** *float[0,1]* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Color1_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Farbindex von Visio oder der RGB-Wert der ersten Farbe.  <br/> |
| _Color2_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Farbindex von Visio oder der RGB-Wert der zweiten Farbe.  <br/> |
| _float[0,1]_ <br/> |Erforderlich  <br/> |**Float** <br/> |Der Anteil, in dem  _Farbe2_ bzw.  _Farbe1_ gemischt werden soll. Eine reelle Zahl zwischen 0 und 1.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **RGB**
  
## <a name="remarks"></a>Bemerkungen

Die zurückgegebene Farbe wird durch die relativen Proportionen bestimmt, in denen  _Farbe2_ bzw.  _Farbe1_ gemischt werden soll, wie durch den  _Float-Parameter_ angegeben. Wenn float beispielsweise 0,25 _ist,_ besteht die zurückgegebene Farbe aus 75 % der _Farbe1_ und 25 % der _Farbe2._ 
  
Eine weitere Möglichkeit, dies zu bedenken, ist, dass der  _Float-Wert_ dem Punkt entlang des Farbspektrums von  _Farbe1_ bis  _Farbe2_ entspricht. Daher erzeugen kleinere Zahlen (näher an Null) für  _Float_ Mischungen, die sich der  _Farbe1_ nähern, während größere Zahlen (näher an 1) Mischungen erzeugen, die sich der  _Farbe2_ nähern.
  

