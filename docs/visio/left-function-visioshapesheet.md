---
title: LEFT Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Gibt das am weitesten links oder die Zeichen in einer Textzeichenfolge, basierend auf der Anzahl der Zeichen an, die Sie angeben.
ms.openlocfilehash: 4e8deb3098ce6d217dcce0cae23d07ed723d9fb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797309"
---
# <a name="left-function-visioshapesheet"></a>LEFT Function (VisioShapeSheet)

Gibt das am weitesten links oder die Zeichen in einer Textzeichenfolge, basierend auf der Anzahl der Zeichen an, die Sie angeben.
  
## <a name="syntax"></a>Syntax

Links (** *Text* **, [, ** *Num_chars_opt* **]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Zeichenfolge mit den zu extrahierenden Zeichen.  <br/> |
| _num_chars_opt_ <br/> |Optional  <br/> |**Numeric** <br/> |Die Anzahl der Zeichen, die extrahiert werden sollen.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Der Wert von _Num_chars_opt_ muss größer als oder gleich 0 (null). 
  
Wenn _Num_chars_opt_ größer als die Länge des Texts ist, gibt links des gesamten Texts. Wenn _Num_chars_opt_ ausgelassen wird, wird angenommen, 1 sein. 
  
## <a name="example"></a>Beispiel

LEFT ("Januar 1, 2004", 3) 
  
Ergibt den Wert Jan. 
  

