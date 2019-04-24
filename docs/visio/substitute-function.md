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
description: Ersetzt einen Teil einer Textzeichenfolge durch eine andere Textzeichenfolge.
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346823"
---
# <a name="substitute-function"></a>SUBSTITUTE Function

Ersetzt einen Teil einer Textzeichenfolge durch eine andere Textzeichenfolge. 
  
## <a name="syntax"></a>Syntax

 Ersatz (* * *Text* * *, * * *old_text* * *, * * *new_text* * * [, * * *start_num* * *] [, * * *ignore_case_opt* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Text oder der Bezug auf eine Zelle mit dem Text, in dem Zeichen ersetzt werden sollen.  <br/> |
| _old_text_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Text, der ersetzt werden soll.  <br/> |
| _new_text_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Text, den Sie zum Ersetzen von _old_text_verwenden möchten.  <br/> |
| _start_num_opt_ <br/> |Optional  <br/> |**Numerisch** <br/> |Gibt an, welche Vorkommen von old_text ersetzt werden sollen.  <br/> |
| _ignore_case_opt_ <br/> |Optional  <br/> |**Boolean** <br/> |FALSE, wenn Groß- und Kleinschreibung zu beachten ist; andernfalls TRUE. Die Standardeinstellung ist FALSE.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

 Wenn Sie _start_num_opt_angeben, wird nur das Vorkommen von _old_text_ ersetzt. Andernfalls wird jedes Vorkommen von _old_text_ in _Text_ in new_text geändert _._
  
Verwenden Sie die SUBSTITUTE-Funktion, wenn bestimmter Text in einer Zeichenfolge ersetzt werden soll. Wenn Sie Text ersetzen möchten, der an einer bestimmten Stelle in einer Textzeichenfolge vorkommt, verwenden Sie die REPLACE-Funktion.
  
## <a name="example"></a>Beispiel

SUBSTITUTE ("1 January 2003", "January", "JAN") 
  
Gibt "1 JAN 2003" zurück. 
  
SUBSTITUTE ("1 January 2003","january","JAN") 
  
Gibt "1 January 2003" zurück. Es wurde keine Änderung durchgeführt, da bei der Textsuche zwischen Groß- und Kleinschreibung unterschieden wird. 
  

