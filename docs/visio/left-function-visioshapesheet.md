---
title: LEFT-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
ms.localizationpriority: medium
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Gibt das zeichenstärkste Zeichen in einer Textzeichenfolge zurück, basierend auf der Anzahl der von Ihnen angegebenen Zeichen.
ms.openlocfilehash: 31b690c231f59bed53b8d04b0a4298621a718101
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554509"
---
# <a name="left-function-visioshapesheet"></a>LEFT-Funktion (VisioShapeSheet)

Gibt das zeichenstärkste Zeichen in einer Textzeichenfolge zurück, basierend auf der Anzahl der von Ihnen angegebenen Zeichen.
  
## <a name="syntax"></a>Syntax

LEFT(** *text* **, [, ** *num_chars_opt* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Zeichenfolge mit den zu extrahierenden Zeichen.  <br/> |
| _num_chars_opt_ <br/> |Optional  <br/> |**Numeric** <br/> |Die Anzahl der Zeichen, die extrahiert werden sollen.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert von  _num_chars_opt_ muss größer oder gleich Null (0) sein. 
  
Wenn  _num_chars_opt_ größer als die Länge des Texts ist, gibt LEFT den gesamten Text zurück. Wenn  _num_chars_opt_ weggelassen wird, wird davon ausgegangen, dass es sich um 1 handelt. 
  
## <a name="example"></a>Beispiel

LEFT ("Januar 1, 2004", 3) 
  
Ergibt den Wert Jan. 
  

