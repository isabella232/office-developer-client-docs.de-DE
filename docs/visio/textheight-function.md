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
description: Gibt die Höhe des zusammengesetzten Texts in einer Form zurück, in der keine Textzeile MaximumWidth überschreitet.
ms.openlocfilehash: 7455f58f14f9a4a0ae1fcd5375dba5d5860d3852
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332353"
---
# <a name="textheight-function"></a>TEXTHÖHE-Funktion

Gibt die Höhe des zusammengesetzten Texts in einer Form zurück, in der keine Textzeile _MaximumWidth_überschreitet. 
  
## <a name="syntax"></a>Syntax

TextHEIGHT (* * *Shapename! DerText* * * * * *[, MaximumWidth]* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Shapename! DerText_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Verweis auf die Zelle mit dem Namen DerText im Ziel-Shape.  _Shapename!_ ist der Name der Form, aus der Sie den Text abrufen möchten.  <br/> |
| _MaximumWidth_ <br/> |Optional  <br/> |**Numerisch** <br/> |Die maximale Breite eines Textblocks.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Der zurückgegebene Wert enthält die Höhe des Texts einschließlich der Abstände vor und hinter dem Text, des Zeilenabstands im Text und der oberen und unteren Textblockränder. Diese Funktion wird meistens verwendet, um die Höhe eines Shapes so anzupassen, dass der gesamte Text vollständig dargestellt wird.
  
## <a name="example"></a>Beispiel

TEXTHEIGHT(TheText,(Width - 0.5 in)) 
  
Gibt die Texthöhe zurück, wenn der Text auf die Breite des Shapes abzüglich 0,5 Zoll umgebrochen wird. 
  

