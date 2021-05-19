---
title: FIND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60101
localization_priority: Normal
ms.assetid: c827ecd4-5593-6d4f-2746-d13b02b098fe
description: Sucht eine Textzeichenfolge, die in einer anderen Textzeichenfolge enthalten ist, und gibt die Anfangsposition der gesuchten Textzeichenfolge relativ zu ihrer Position in der Textzeichenfolge zurück, die sie enthält.
ms.openlocfilehash: 40d65af25d89774c1bdf7b235cf653dbb61dd1c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426576"
---
# <a name="find-function"></a>FIND Function

Sucht eine Textzeichenfolge, die in einer anderen Textzeichenfolge enthalten ist, und gibt die Anfangsposition der gesuchten Textzeichenfolge relativ zu ihrer Position in der Textzeichenfolge zurück, die sie enthält.
  
## <a name="syntax"></a>Syntax

FIND (** *find_text* **, ** *within_text* **,[ ** *start_num* ** ], [ ** *ignore_case* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _find_text_ <br/> |Erforderlich  <br/> |**String** <br/> |Die gesuchte Zeichenfolge.  <br/> |
| _format_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Zeichenfolge, die den gesuchten Text enthält.  <br/> |
| _start_num_ <br/> |Optional.  <br/> |**Number** <br/> |Das Zeichen, bei dem die Suche beginnen soll. Das erste Zeichen in  _within_text_ ist 1. Wenn  _start_num_ fehlt, wird angenommen, dass es 1 ist.  <br/> |
| _ignore_case_ <br/> |Optional  <br/> |**Boolescher Wert** <br/> |In der Standardeinstellung ist bei der FIND-Funktion Groß- und Kleinschreibung zu beachten. Wenn die Groß- und Kleinschreibung ignoriert werden soll, legen Sie für dieses Argument den Wert TRUE fest.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Nummer
  
## <a name="remarks"></a>Hinweise

Wenn mehrere Übereinstimmungen gefunden werden, gibt FIND die Anfangsposition der ersten Übereinstimmung in der Zeichenfolge zurück. Das  _find_text-Argument_ sieht keine Zeichen als Platzhalter an. 
  
Wenn  _find_text_:
  
-  Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1). 
    
- Wird nicht  _in_ within_text angezeigt, gibt FIND die #VALUE! Ist dies nicht der Fall, gibt INDEX den Fehlerwert #REF! zurück. 
    
Wenn  _start_num_:
  
- nicht größer als 0 (null) ist, gibt FIND den Fehlerwert #WERT! zurück. 
    
- Ist größer als die Länge der  _within_text_, gibt FIN die #VALUE! zurück. 
    
## <a name="example"></a>Beispiel

FIND ("2003","Januar 1, 2003") 
  
Gibt 12 zurück. 
  

