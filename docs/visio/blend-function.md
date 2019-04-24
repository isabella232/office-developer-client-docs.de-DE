---
title: BLEND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Fügt zwei Farben in den durch den Parameter float angegebenen Anteil ein.
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303297"
---
# <a name="blend-function"></a>BLEND Function

Fügt zwei Farben in den durch den Parameter _float_ angegebenen Anteil ein. 
  
## <a name="syntax"></a>Syntax

BLEND (* * *color1* * *, * * *color2* * *, * * *float [0, 1]* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _color1_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Der Farbindex von Visio oder der RGB-Wert der ersten Farbe.  <br/> |
| _color2_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Der Farbindex von Visio oder der RGB-Wert der zweiten Farbe.  <br/> |
| _float [0, 1]_ <br/> |Erforderlich  <br/> |**Float** <br/> |Der Anteil, in dem _color2_ und _color1_. Eine reelle Zahl zwischen 0 und 1.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **RGB**
  
## <a name="remarks"></a>Bemerkungen

Die zurückgegebene Farbe wird durch die relativen Proportionen bestimmt, in denen _color2_ und _color1_, wie durch den _float_ -Parameter angegeben, gemischt werden sollen. Wenn _float_ beispielsweise 0,25 ist, besteht die zurückgegebene farbe aus 75% aus _color1_ und 25% aus _color2_. 
  
Eine andere Möglichkeit, darüber nachzudenken, ist, dass der _float_ -Wert dem Punkt entlang des Farbspektrums von _color1_ zu _color2_entspricht. Daher werden kleinere Zahlen (näher an null) für _float_ -Produkte näher an _color1_angeglichen, während größere Zahlen (näher bei 1) eine Verschmelzung näher an _color2_erzeugen.
  

