---
title: MID Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Gibt eine bestimmte Anzahl von Zeichen aus einer Textzeichenfolge zurückgegeben, beginnend bei der Position, die Sie angeben, die anhand der Anzahl der Zeichen, die Sie angeben.
ms.openlocfilehash: 96e697211ebf6ea61ddf0b749d8e1259f2a1e53d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797526"
---
# <a name="mid-function-visioshapesheet"></a>MID Function (VisioShapeSheet)

Gibt eine bestimmte Anzahl von Zeichen aus einer Textzeichenfolge zurückgegeben, beginnend bei der Position, die Sie angeben, die anhand der Anzahl der Zeichen, die Sie angeben.
  
## <a name="syntax"></a>Syntax

MID (** *Text* **, ** *Erstes_Zeichen* **, ** *Num_chars* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Zeichenfolge mit den zu extrahierenden Zeichen.  <br/> |
| _Erstes_Zeichen_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die Position des ersten Zeichens, das extrahiert werden soll. Das erste Zeichen in der Zeichenfolge ist Position 1.  <br/> |
| _Anzahl_Zeichen_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die Anzahl der Zeichen, die zurückgegeben werden sollen.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Wenn *start_num* 
  
- Größer als die Länge von *Text* , gibt MID "" (leere Zeichenfolge). 
    
- Kleiner als die Länge von *Text* , aber *Start_num* plus *Num_chars* die Länge des *Textes* überschreitet, gibt MID die Zeichen bis zum Ende des *Texts* zurück. 
    
- kleiner als 1 ist, gibt MID den Fehlerwert #WERT! zurück. 
    
Wenn *Num_chars* negativ ist, gibt MID den #VALUE! Fehlerwert. 
  
## <a name="example"></a>Beispiel

MID ("SSN 999-99-9999",5,11) 
  
Gibt 999-99-9999 zurück. 
  

