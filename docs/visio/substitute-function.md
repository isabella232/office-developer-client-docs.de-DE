---
title: SUBSTITUTE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60115
localization_priority: Normal
ms.assetid: 4a27663a-9d37-2ac4-5856-edeb0880f16e
description: Ersetzt einen Teil einer Zeichenfolge durch eine andere Textzeichenfolge.
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 4590b7ed906d008693a58abe63f089ed8a380b34
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2018
ms.locfileid: "26643213"
---
# <a name="substitute-function"></a>SUBSTITUTE Function

Ersetzt einen Teil einer Zeichenfolge durch eine andere Textzeichenfolge. 
  
## <a name="syntax"></a>Syntax

 Ersatz (** *Text* **, ** *Alter_Text* **, ** *Neuer_Text* ** [, ** *Erstes_Zeichen* **] [, ** *Ignore_case_opt* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Text oder der Bezug auf eine Zelle mit dem Text, in dem Zeichen ersetzt werden sollen.  <br/> |
| _Alter_Text_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Text, der ersetzt werden soll.
  <br/> |
| _Neuer_Text_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Text, den Sie _Alter_Text_ersetzen möchten.  <br/> |
| _start_num_opt_ <br/> |Optional  <br/> |**Numerisch** <br/> |Gibt an, welche Vorkommen von Old_text ersetzt werden soll.  <br/> |
| _ignore_case_opt_ <br/> |Optional  <br/> |**Boolean** <br/> |FALSE, wenn Groß- und Kleinschreibung zu beachten ist; andernfalls TRUE. Die Standardeinstellung ist FALSE.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Hinweise

 Wenn Sie _Start_num_opt_angeben, wird nur dieses Auftreten von _Old_text_ ersetzt. Andernfalls wird jedes Vorkommen von _Old_text_ in _Text_ um geändert _Neuer_Text._
  
Verwenden Sie die Ersatz-Funktion, wenn Sie bestimmten Text in einer Zeichenfolge ersetzen möchten. Wenn Text zu ersetzen, das auftritt, an einer bestimmten Stelle in einer Textzeichenfolge zurückgegeben werden soll, verwenden Sie die REPLACE-Funktion.
  
## <a name="example"></a>Beispiel

SUBSTITUTE ("1 January 2003", "January", "JAN") 
  
Gibt "1 JAN 2003" zurück. 
  
SUBSTITUTE ("1 January 2003","january","JAN") 
  
Gibt "1. Januar 2003" zurück. Keine Änderung erfolgt, da die Textsuche Groß-/Kleinschreibung beachtet wird. 
  

