---
title: RIGHT-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
ms.localizationpriority: medium
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Gibt das letzte Zeichen in einer Textzeichenfolge basierend auf der Anzahl der von Ihnen angegebenen Zeichen zurück.
ms.openlocfilehash: 4b4a2cb68f6e15989fade7088e887f852ac4eee8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573516"
---
# <a name="right-function-visioshapesheet"></a>RIGHT-Funktion (VisioShapeSheet)

Gibt das letzte Zeichen in einer Textzeichenfolge basierend auf der Anzahl der von Ihnen angegebenen Zeichen zurück.
  
## <a name="syntax"></a>Syntax

RIGHT(** *text* ** [, ** *num_chars_opt* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> | Die Textzeichenfolge mit den zu extrahierenden Zeichen.  <br/> |
| _num_chars_opt_ <br/> |Optional  <br/> |**Number** <br/> |Die Anzahl der Zeichen, die extrahiert werden sollen. Standardwert ist 1.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert von  _num_chars_opt_ muss größer oder gleich Null (0) sein. 
  
Wenn  _num_chars_opt_ größer als die Länge des Texts ist, gibt RIGHT den gesamten Text zurück. Wenn  _num_chars_opt_ weggelassen wird, wird davon ausgegangen, dass es sich um 1 handelt. 
  
## <a name="example"></a>Beispiel

RIGHT ("Januar 1, 2004", 4) 
  
Gibt den Wert 2004 zurück. 
  

