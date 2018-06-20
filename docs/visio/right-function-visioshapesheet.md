---
title: RIGHT Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
localization_priority: Normal
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Gibt das letzte Zeichen oder Zeichen in einer Textzeichenfolge, basierend auf der Anzahl der Zeichen an, die Sie angeben.
ms.openlocfilehash: e35cc4918809d5f134f9519c01cb3c93407258e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797855"
---
# <a name="right-function-visioshapesheet"></a>RIGHT Function (VisioShapeSheet)

Gibt das letzte Zeichen oder Zeichen in einer Textzeichenfolge, basierend auf der Anzahl der Zeichen an, die Sie angeben.
  
## <a name="syntax"></a>Syntax

RECHTS (** *Text* ** [, ** *Num_chars_opt* **]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> | Die Textzeichenfolge mit den zu extrahierenden Zeichen.  <br/> |
| _num_chars_opt_ <br/> |Optional  <br/> |**Nummer** <br/> |Die Anzahl der Zeichen, die extrahiert werden sollen. Standardwert ist 1.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

String
  
## <a name="remarks"></a>Hinweise

Der Wert von _Num_chars_opt_ muss größer als oder gleich 0 (null). 
  
Wenn _Num_chars_opt_ größer als die Länge des Texts ist, gibt rechts des gesamten Texts. Wenn _Num_chars_opt_ ausgelassen wird, wird angenommen, 1 sein. 
  
## <a name="example"></a>Beispiel

RIGHT ("Januar 1, 2004", 4) 
  
Gibt den Wert 2004 zurück. 
  

