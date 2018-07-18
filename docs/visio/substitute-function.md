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
ms.openlocfilehash: 2c33d8aafbd68054ac39d14bb4fb3cf857fb367e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798216"
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
| _start_num_opt_ <br/> |Optional  <br/> |**Numeric** <br/> |Gibt an, welche Vorkommen von old_text ersetzt werden sollen.  <br/> |
| _ignore_case_opt_ <br/> |Optional  <br/> |**Boolean** <br/> |FALSE, wenn Groß- und Kleinschreibung zu beachten ist; andernfalls TRUE. Die Standardeinstellung ist FALSE.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

 Wenn Sie _Start_num_opt_angeben, wird nur dieses Auftreten von _Old_text_ ersetzt. Andernfalls wird jedes Vorkommen von _Old_text_ in _Text_ um geändert _Neuer_Text._
  
Verwenden Sie die Ersatz-Funktion, wenn Sie bestimmten Text in einer Zeichenfolge ersetzen möchten. Wenn Text zu ersetzen, das auftritt, an einer bestimmten Stelle in einer Textzeichenfolge zurückgegeben werden soll, verwenden Sie die REPLACE-Funktion.
  
## <a name="example"></a>Beispiel

SUBSTITUTE ("1 January 2003", "January", "JAN") 
  
Gibt "1 JAN 2003" zurück. 
  
SUBSTITUTE ("1 January 2003","january","JAN") 
  
Gibt "1. Januar 2003" zurück. Keine Änderung erfolgt, da die Textsuche Groß-/Kleinschreibung beachtet wird. 
  

