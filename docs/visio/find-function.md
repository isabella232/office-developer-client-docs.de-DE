---
title: FIND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60101
ms.localizationpriority: medium
ms.assetid: c827ecd4-5593-6d4f-2746-d13b02b098fe
description: Sucht eine Textzeichenfolge, die in einer anderen Textzeichenfolge enthalten ist, und gibt die Anfangsposition der Textzeichenfolge zurück, die Sie relativ zu ihrer Position in der Textzeichenfolge suchen, die sie enthält.
ms.openlocfilehash: 313f6b97c5aacbb83e8aeedb91b69ce28cef465a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590198"
---
# <a name="find-function"></a>FIND Function

Sucht eine Textzeichenfolge, die in einer anderen Textzeichenfolge enthalten ist, und gibt die Anfangsposition der Textzeichenfolge zurück, die Sie relativ zu ihrer Position in der Textzeichenfolge suchen, die sie enthält.
  
## <a name="syntax"></a>Syntax

FIND (** *find_text* **, ** *within_text* **,[ ** *start_num* ** ], [ ** *ignore_case* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _find_text_ <br/> |Erforderlich  <br/> |**String** <br/> |Die gesuchte Zeichenfolge.  <br/> |
| _format_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Zeichenfolge, die den gesuchten Text enthält.  <br/> |
| _start_num_ <br/> |Optional  <br/> |**Number** <br/> |Das Zeichen, bei dem die Suche beginnen soll. Das erste Zeichen in  _within_text_ ist 1. Wenn  _start_num_ fehlt, wird der Wert 1 angenommen.  <br/> |
| _ignore_case_ <br/> |Optional  <br/> |**Boolescher Wert** <br/> |In der Standardeinstellung ist bei der FIND-Funktion Groß- und Kleinschreibung zu beachten. Wenn die Groß- und Kleinschreibung ignoriert werden soll, legen Sie für dieses Argument den Wert TRUE fest.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zahl
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn mehrere Übereinstimmungen gefunden werden, gibt FIND die Anfangsposition der ersten Übereinstimmung in der Zeichenfolge zurück. Das  _argument find_text_ betrachtet keine Zeichen als Platzhalter. 
  
Wenn _find_text:_
  
-  Ist leer (""), stimmt FIND mit dem ersten Zeichen in der Suchzeichenfolge überein (d. a. dem  _Zeichen,_ das start_num oder 1 nummeriert ist). 
    
- Wird in  _within_text_ nicht angezeigt, gibt FIND die #VALUE zurück! Ist dies nicht der Fall, gibt INDEX den Fehlerwert #REF! zurück. 
    
Wenn _start_num:_
  
- nicht größer als 0 (null) ist, gibt FIND den Fehlerwert #WERT! zurück. 
    
- Ist größer als die Länge der  _within_text_, gibt FINDreturns die #VALUE! zurück. 
    
## <a name="example"></a>Beispiel

FIND ("2003","Januar 1, 2003") 
  
Gibt 12 zurück. 
  

