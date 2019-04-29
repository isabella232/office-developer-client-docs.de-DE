---
title: LEFT-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Gibt die am weitesten links liegenden Zeichen oder Zeichen in einer Textzeichenfolge basierend auf der Anzahl der Zeichen zurück, die Sie angeben.
ms.openlocfilehash: aa4141cfc53bd41a6d58e8bc666b18a06fc80245
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427521"
---
# <a name="left-function-visioshapesheet"></a>LEFT-Funktion (VisioShapeSheet)

Gibt die am weitesten links liegenden Zeichen oder Zeichen in einer Textzeichenfolge basierend auf der Anzahl der Zeichen zurück, die Sie angeben.
  
## <a name="syntax"></a>Syntax

Left (* * *Text* * *, [, * * *num_chars_opt* * *]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Zeichenfolge mit den zu extrahierenden Zeichen.  <br/> |
| _num_chars_opt_ <br/> |Optional  <br/> |**Numeric** <br/> |Die Anzahl der Zeichen, die extrahiert werden sollen.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Der Wert von _num_chars_opt_ muss größer oder gleich NULL (0) sein. 
  
Wenn _num_chars_opt_ größer als die Länge des Texts ist, gibt Left den gesamten Text zurück. Wenn _num_chars_opt_ ausgelassen wird, wird davon ausgegangen, dass es 1 ist. 
  
## <a name="example"></a>Beispiel

LEFT ("Januar 1, 2004", 3) 
  
Ergibt den Wert Jan. 
  

