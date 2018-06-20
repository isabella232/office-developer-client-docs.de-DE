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
description: Sucht eine Zeichenfolge innerhalb einer anderen Zeichenfolge und gibt die Startposition der gesuchten relativ zu seiner Position in der Zeichenfolge, die er enthält Textzeichenfolge zurück.
ms.openlocfilehash: e29e8e89418f0162cae0ec9904c2205218e799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797036"
---
# <a name="find-function"></a>FIND-Funktion

Sucht eine Zeichenfolge innerhalb einer anderen Zeichenfolge und gibt die Startposition der gesuchten relativ zu seiner Position in der Zeichenfolge, die er enthält Textzeichenfolge zurück.
  
## <a name="syntax"></a>Syntax

Suchen Sie nach (** *Suchtext* **, ** *Within_text* **, [** *Erstes_Zeichen* **], [** *Ignore_case* **]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Suchtext_ <br/> |Erforderlich  <br/> |**String** <br/> |Die gesuchte Zeichenfolge.  <br/> |
| _format_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Zeichenfolge, die den gesuchten Text enthält.  <br/> |
| _Erstes_Zeichen_ <br/> |Optional  <br/> |**Nummer** <br/> |Das Zeichen, für die Suche zu starten. Das erste Zeichen in _Within_text_ ist 1. Wenn _Start_num_ nicht vorhanden ist, wird angenommen, 1 sein.  <br/> |
| _ignore_case_ <br/> |Optional  <br/> |**Boolean** <br/> |In der Standardeinstellung ist bei der FIND-Funktion Groß- und Kleinschreibung zu beachten. Wenn die Groß- und Kleinschreibung ignoriert werden soll, legen Sie für dieses Argument den Wert TRUE fest.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zahl
  
## <a name="remarks"></a>Hinweise

Wenn mehrere Übereinstimmungen gefunden werden, gibt die FIND-Funktion die Anfangsposition der die erste Übereinstimmung in der Zeichenfolge. Das Argument _Suchtext_ berücksichtigt Zeichen als Platzhalter werden nicht. 
  
Wenn _Suchtext_:
  
-  Ist leer (""), suchen entspricht das erste Zeichen in der Suchzeichenfolge (d. h., das Zeichen mit dem _Erstes_Zeichen_ oder 1). 
    
- Erscheint nicht in _Within_text_, FIND gibt die #VALUE! Fehlerwert. 
    
Wenn _Start_num_:
  
- nicht größer als 0 (null) ist, gibt FIND den Fehlerwert #WERT! zurück. 
    
- Ist größer als die Länge von _Text ist_, gibt die #VALUE! Fehlerwert. 
    
## <a name="example"></a>Beispiel

FIND ("2003","Januar 1, 2003") 
  
Gibt 12 zurück. 
  

