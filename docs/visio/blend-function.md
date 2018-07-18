---
title: BLEND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Mischt zwei Farben in dem Verhältnis, das vom Float-Parameter angegeben.
ms.openlocfilehash: 61993cea9eed6583d62004e1c756368b67c7bb33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796522"
---
# <a name="blend-function"></a>BLEND Function

Mischt zwei Farben in dem Verhältnis, das vom _Float_ -Parameter angegeben. 
  
## <a name="syntax"></a>Syntax

BLEND (** *color1* **, ** *color2* **, ** *Float [0,1]* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _color1_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Farbindex von Visio oder der RGB-Wert der ersten Farbe.  <br/> |
| _color2_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Farbindex von Visio oder der RGB-Wert der zweiten Farbe.  <br/> |
| _Float [0,1]_ <br/> |Erforderlich  <br/> |**Float** <br/> |Das Verhältnis, in dem _color2_ und _color1_, jeweils gemischt. Eine reelle Zahl zwischen 0 und 1.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

 **RGB**
  
## <a name="remarks"></a>Bemerkungen

Die zurückgegebene Farbe wird durch die relativen Proportionen in dem _color2_ und _color1_, als vom _Float_ -Parameter angegebenen gemischt bestimmt. Beispielsweise ist _Float_ 0,25, die zurückgegebene Farbe zusammengesetzten 75 % der _color1_ und 25 % der _color2_. 
  
Eine andere Möglichkeit, denken ist, dass der Punkt entlang der Color-Spektrum von _color1_ _color2_ _Float_ -Wert entspricht. Aus diesem Grund Zahlen kleiner (näher null) für _Float_ erzeugen Farbverlauf näher zu _color1_, während größere (näher 1) Zahlen Farbverlauf näher zu _color2_erstellen.
  

