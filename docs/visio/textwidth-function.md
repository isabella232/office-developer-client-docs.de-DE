---
title: TEXTWIDTH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251505
localization_priority: Normal
ms.assetid: a9b8efcf-edc0-ad99-deae-21df16c58807
description: Gibt die Breite des zusammengesetzten Texts in einem Shape zurück.
ms.openlocfilehash: 43848bba4d24a0c31a3a084d123cd56140bf0709
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422033"
---
# <a name="textwidth-function"></a>TEXTWIDTH Function

Gibt die Breite des zusammengesetzten Texts in einem Shape zurück. 
  
## <a name="syntax"></a>Syntax

TextWIDTH (* * *Shapename! DerText* * * * * *[, MaximumWidth]* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Shapename! DerText_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Verweis auf die Zelle mit dem Namen DerText im Ziel-Shape.  _Shapename!_ ist der Name der Form, aus der Sie den Text abrufen möchten.  <br/> |
| _MaximumWidth_ <br/> |Optional  <br/> |**Numeric** <br/> |Die maximale Breite eines Textblocks.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Die TEXTWIDTH-Funktion wird meistens verwendet, um die Breite eines Shapes so anzupassen, dass der enthaltene Text vollständig hineinpasst.
  
Wenn _Sheetn!_ nicht angegeben ist, ist die Standardform die aktuelle Form. 
  
Wenn _MaximumWidth_ angegeben wird, ist das Ergebnis die längste Textzeile, die in _MaximumWidth_passt. Wenn _MaximumWidth_ ausgelassen wird, ist das Ergebnis die Gesamtbreite des Texts. 
  
## <a name="example"></a>Beispiel

TextWIDTH (DerText) 
  
Gibt die Gesamtlänge des Texts im aktuellen Shape zurück. 
  

