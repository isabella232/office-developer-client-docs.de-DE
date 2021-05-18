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
description: Gibt die Breite des zusammengesetzten Texts in einer Form zurück.
ms.openlocfilehash: 43848bba4d24a0c31a3a084d123cd56140bf0709
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422033"
---
# <a name="textwidth-function"></a>TEXTWIDTH Function

Gibt die Breite des zusammengesetzten Texts in einer Form zurück. 
  
## <a name="syntax"></a>Syntax

TEXTWIDTH(** *shapename! TheText* ** ** *[,maximumwidth]* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Verweis auf die Zelle mit dem Namen TheText in der Zielform.  _shapename!_ ist der Name der Form, aus der Sie den Text abrufen möchten.  <br/> |
| _maximumwidth_ <br/> |Optional.  <br/> |**Numeric** <br/> |Die maximale Breite eines Textblocks.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Hinweise

Die TEXTWIDTH-Funktion wird meistens verwendet, um die Breite eines Shapes so anzupassen, dass der enthaltene Text vollständig hineinpasst.
  
Wenn  _sheetN!_ wird nicht angegeben, ist die Standardform die aktuelle Form. 
  
Wenn _maximumwidth_ angegeben wird, ist das Ergebnis die längste Textzeile, die innerhalb von _Maximumwidth liegt._ Wenn  _maximumwidth_ nicht angegeben wird, ist das Ergebnis die Gesamtbreite des Texts. 
  
## <a name="example"></a>Beispiel

TEXTWIDTH(TheText) 
  
Gibt die Gesamtlänge des Texts im aktuellen Shape zurück. 
  

