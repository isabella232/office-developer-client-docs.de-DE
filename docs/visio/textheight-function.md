---
title: TEXTHEIGHT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251504
localization_priority: Normal
ms.assetid: 5a10892f-c8fa-c127-2f5a-564009ce5411
description: Gibt die Höhe des zusammengesetzten Texts in einem Shape zurück, in dem keine Textzeile maxBreite überschreitet.
ms.openlocfilehash: 9a80dafcf80a1dcba968a0f60465aae4e2a2758b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798252"
---
# <a name="textheight-function"></a>TEXTHÖHE-Funktion

Gibt die Höhe des zusammengesetzten Texts in einem Shape zurück, in dem keine Textzeile _maxBreite_überschreitet. 
  
## <a name="syntax"></a>Syntax

TEXTHEIGHT (** *Shapename! TheText* ** ** *[, maxBreite]* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Shapename! TheText_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Verweis auf die Zelle TheText mit der in der Ziel-Shape.  _Shapename!_ ist der Name des Shapes, von dem Sie den Text abrufen möchten.  <br/> |
| _maxBreite_ <br/> |Optional  <br/> |**Numeric** <br/> |Die maximale Breite eines Textblocks.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Der zurückgegebene Wert enthält die Höhe des Texts einschließlich der Abstände vor und hinter dem Text, des Zeilenabstands im Text und der oberen und unteren Textblockränder. Diese Funktion wird meistens verwendet, um die Höhe eines Shapes so anzupassen, dass der gesamte Text vollständig dargestellt wird.
  
## <a name="example"></a>Beispiel

TEXTHEIGHT(TheText,(Width - 0.5 in)) 
  
Gibt die Texthöhe zurück, wenn der Text auf die Breite des Shapes abzüglich 0,5 Zoll umgebrochen wird. 
  

