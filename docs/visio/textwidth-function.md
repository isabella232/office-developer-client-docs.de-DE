---
title: TEXTWIDTH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251505
ms.localizationpriority: medium
ms.assetid: a9b8efcf-edc0-ad99-deae-21df16c58807
description: Gibt die Breite des zusammengesetzten Texts in einer Form zurück.
ms.openlocfilehash: 7db00c5d7d0c1e984bb18e786364569afe0ec0e0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627338"
---
# <a name="textwidth-function"></a>TEXTWIDTH Function

Gibt die Breite des zusammengesetzten Texts in einer Form zurück. 
  
## <a name="syntax"></a>Syntax

TEXTWIDTH(** *shapename! TheText* ** ** *[,maximumwidth]* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Verweis auf die Zelle mit dem Namen "TheText" im Ziel-Shape.  _Shapename!_ ist der Name des Shapes, aus dem der Text abgerufen werden soll.  <br/> |
| _maximumwidth_ <br/> |Optional  <br/> |**Numeric** <br/> |Die maximale Breite eines Textblocks.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Die TEXTWIDTH-Funktion wird meistens verwendet, um die Breite eines Shapes so anzupassen, dass der enthaltene Text vollständig hineinpasst.
  
Wenn  _sheetN!_ wird weggelassen, die Standardform ist die aktuelle Form. 
  
Wenn  _maximumwidth_ angegeben wird, ist das Ergebnis die längste Textzeile, die in  _maximumwidth_ passt. Wenn  _MaximumWidth_ nicht angegeben wird, ergibt sich die Gesamtbreite des Texts. 
  
## <a name="example"></a>Beispiel

TEXTWIDTH(TheText) 
  
Gibt die Gesamtlänge des Texts im aktuellen Shape zurück. 
  

