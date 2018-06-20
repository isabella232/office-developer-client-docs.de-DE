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
ms.openlocfilehash: d96b9489c08ce38205f8e9ad91e361fcb643c39c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798250"
---
# <a name="textwidth-function"></a>TEXTWIDTH Function

Gibt die Breite des zusammengesetzten Texts in einem Shape zurück. 
  
## <a name="syntax"></a>Syntax

TEXTWIDTH (** *Shapename! TheText* ** ** *[, maxBreite]* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Shapename! TheText_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Verweis auf die Zelle TheText mit der in der Ziel-Shape.  _Shapename!_ ist der Name des Shapes, von dem Sie den Text abrufen möchten.  <br/> |
| _maxBreite_ <br/> |Optional  <br/> |**Numerische** <br/> |Die maximale Breite eines Textblocks.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

String
  
## <a name="remarks"></a>Bemerkungen

Die TEXTWIDTH-Funktion wird meistens verwendet, um die Breite eines Shapes so anzupassen, dass der enthaltene Text vollständig hineinpasst.
  
Wenn _SheetN!_ wird Length angegeben, das Standard-Shape ist das aktuelle Shape. 
  
Wenn _maxBreite_ angegeben ist, ist das Ergebnis der längsten Textzeile in _maxBreite_hineinpasst. Wenn _maxBreite_ ausgelassen wird, ist das Ergebnis die gesamte Breite des Texts. 
  
## <a name="example"></a>Beispiel

(TEXTWIDTH(DerText) 
  
Gibt die Gesamtlänge des Texts im aktuellen Shape zurück. 
  

