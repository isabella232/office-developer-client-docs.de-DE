---
title: MID-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Gibt eine bestimmte Anzahl von Zeichen aus einer Textzeichenfolge zurück, beginnend bei der angegebenen Position, basierend auf der Anzahl der Zeichen, die Sie angeben.
ms.openlocfilehash: 58d5e784e49c8e9fba0bf668626049298783c158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410266"
---
# <a name="mid-function-visioshapesheet"></a>MID-Funktion (VisioShapeSheet)

Gibt eine bestimmte Anzahl von Zeichen aus einer Textzeichenfolge zurück, beginnend bei der angegebenen Position, basierend auf der Anzahl der Zeichen, die Sie angeben.
  
## <a name="syntax"></a>Syntax

MID (* * *Text* * *, * * *start_num* * *, * * *num_chars* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Zeichenfolge mit den zu extrahierenden Zeichen.  <br/> |
| _start_num_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Position des ersten Zeichens, das extrahiert werden soll. Das erste Zeichen in der Zeichenfolge ist Position 1.  <br/> |
| _num_chars_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Anzahl der Zeichen, die zurückgegeben werden sollen.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Wenn *start_num* ist: 
  
- Größer als die Länge des *Texts* , Mid gibt "" (leeren Text) zurück. 
    
- Kleiner als die Länge des *Texts* , aber *start_num* Plus *num_chars* überschreitet die Länge ** des Texts, Mid gibt die Zeichen bis zum Ende des *Texts* zurück. 
    
- kleiner als 1 ist, gibt MID den Fehlerwert #WERT! zurück. 
    
Wenn *num_chars* negativ ist, gibt MID den #VALUE zurück. zurück. 
  
## <a name="example"></a>Beispiel

MID ("SSN 999-99-9999",5,11) 
  
Gibt 999-99-9999 zurück. 
  

