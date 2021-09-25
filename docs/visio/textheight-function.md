---
title: TEXTHEIGHT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251504
ms.localizationpriority: medium
ms.assetid: 5a10892f-c8fa-c127-2f5a-564009ce5411
description: Gibt die Höhe des zusammengesetzten Texts in einer Form zurück, bei der keine Textzeile die maximale Breite überschreitet.
ms.openlocfilehash: 2d6425aa3003ccee3cd5441f7408074256acf8b4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597877"
---
# <a name="textheight-function"></a>TEXTHÖHE-Funktion

Gibt die Höhe des zusammengesetzten Texts in einer Form zurück, bei der keine Textzeile die  _maximale Breite_ überschreitet. 
  
## <a name="syntax"></a>Syntax

TEXTHEIGHT(** *shapename! TheText* ** ** *[,maximumwidth]* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Verweis auf die Zelle mit dem Namen "TheText" im Ziel-Shape.  _Shapename!_ ist der Name des Shapes, aus dem der Text abgerufen werden soll.  <br/> |
| _maximumwidth_ <br/> |Optional  <br/> |**Numeric** <br/> |Die maximale Breite eines Textblocks.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>HinwBemerkungeneise

Der zurückgegebene Wert enthält die Höhe des Texts einschließlich der Abstände vor und hinter dem Text, des Zeilenabstands im Text und der oberen und unteren Textblockränder. Diese Funktion wird meistens verwendet, um die Höhe eines Shapes so anzupassen, dass der gesamte Text vollständig dargestellt wird.
  
## <a name="example"></a>Beispiel

TEXTHEIGHT(TheText,(Width - 0.5 in)) 
  
Gibt die Texthöhe zurück, wenn der Text auf die Breite des Shapes abzüglich 0,5 Zoll umgebrochen wird. 
  

