---
title: MID-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
ms.localizationpriority: medium
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Gibt eine bestimmte Anzahl von Zeichen aus einer Textzeichenfolge zurück, beginnend an der von Ihnen angegebenen Position, basierend auf der Anzahl der angegebenen Zeichen.
ms.openlocfilehash: 7813f123ccd349c3122aa02449f5ed5d9a7038a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623341"
---
# <a name="mid-function-visioshapesheet"></a>MID-Funktion (VisioShapeSheet)

Gibt eine bestimmte Anzahl von Zeichen aus einer Textzeichenfolge zurück, beginnend an der von Ihnen angegebenen Position, basierend auf der Anzahl der angegebenen Zeichen.
  
## <a name="syntax"></a>Syntax

MID (** *text* **, ** *start_num* **, ** *num_chars* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Zeichenfolge mit den zu extrahierenden Zeichen.  <br/> |
| _start_num_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Position des ersten Zeichens, das extrahiert werden soll. Das erste Zeichen in der Zeichenfolge ist Position 1.  <br/> |
| _Anzahl_zeichen_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Anzahl der Zeichen, die zurückgegeben werden sollen.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Wenn *start_num:* 
  
- Größer als die Textlänge  *,*  gibt MID "" (leerer Text) zurück. 
    
- Kleiner als die  Textlänge, aber *start_num* plus *num_chars* die Textlänge überschreitet,  gibt MID die Zeichen bis zum Ende des *Texts* zurück. 
    
- kleiner als 1 ist, gibt MID den Fehlerwert #WERT! zurück. 
    
Wenn  *num_chars*  negativ ist, gibt MID die #VALUE zurück! zurück. 
  
## <a name="example"></a>Beispiel

MID ("SSN 999-99-9999",5,11) 
  
Gibt 999-99-9999 zurück. 
  

