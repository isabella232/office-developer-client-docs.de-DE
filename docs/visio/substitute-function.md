---
title: SUBSTITUTE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60115
ms.localizationpriority: medium
ms.assetid: 4a27663a-9d37-2ac4-5856-edeb0880f16e
description: Ersetzt einen Teil einer Textzeichenfolge durch eine andere Textzeichenfolge.
ms.openlocfilehash: 88aeaff349e24d1b6a7e04470061e756acf6598e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559423"
---
# <a name="substitute-function"></a>SUBSTITUTE Function

Ersetzt einen Teil einer Textzeichenfolge durch eine andere Textzeichenfolge. 
  
## <a name="syntax"></a>Syntax

 SUBSTITUTE (** *text* **, ** *old_text* **, ** *new_text* ** [, ** *start_num* ** ][, ** *ignore_case_opt* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Text oder der Bezug auf eine Zelle mit dem Text, in dem Zeichen ersetzt werden sollen.  <br/> |
| _old_text_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Text, der ersetzt werden soll.  <br/> |
| _new_text_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Text, den Sie verwenden möchten, um  _old_text_ zu ersetzen.  <br/> |
| _start_num_opt_ <br/> |Optional  <br/> |**Numeric** <br/> |Gibt an, welche Vorkommen von old_text ersetzt werden sollen.  <br/> |
| _ignore_case_opt_ <br/> |Optional  <br/> |**Boolescher Wert** <br/> |FALSE, wenn Groß- und Kleinschreibung zu beachten ist; andernfalls TRUE. Die Standardeinstellung ist FALSE.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>HinwBemerkungeneise

 Wenn Sie  _start_num_opt_ angeben, wird nur das Vorkommen von  _old_text_ ersetzt. Andernfalls wird jedes Vorkommen von  _old_text_ im  _Text_ in  _new_text geändert._
  
Verwenden Sie die SUBSTITUTE-Funktion, wenn bestimmter Text in einer Zeichenfolge ersetzt werden soll. Wenn Sie Text ersetzen möchten, der an einer bestimmten Stelle in einer Textzeichenfolge vorkommt, verwenden Sie die REPLACE-Funktion.
  
## <a name="example"></a>Beispiel

SUBSTITUTE ("1 January 2003", "January", "JAN") 
  
Gibt "1 JAN 2003" zurück. 
  
SUBSTITUTE ("1 January 2003","january","JAN") 
  
Gibt "1 January 2003" zurück. Es wurde keine Änderung durchgeführt, da bei der Textsuche zwischen Groß- und Kleinschreibung unterschieden wird. 
  

