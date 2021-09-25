---
title: BITAND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251398
ms.localizationpriority: medium
ms.assetid: c437de23-d2e0-469d-62e6-8eb8b8cfea5c
description: Gibt eine 16-Bit-Binärzahl zurück, bei der jedes Bit nur auf 1 festgelegt ist, wenn das entsprechende Bit in binärer Zahl1 und binärer Zahl2 1 ist. Andernfalls wird das Bit auf 0 festgelegt.
ms.openlocfilehash: ed0844dada0160cd8150762482c8d3b17742ec6b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628773"
---
# <a name="bitand-function"></a>BITAND Function

Gibt eine 16-Bit-Binärzahl zurück, bei der jedes Bit nur auf 1 festgelegt ist, wenn das entsprechende Bit in binärer Zahl1 und binärer Zahl2 1 ist. Andernfalls wird das Bit auf 0 festgelegt. 
  
## <a name="syntax"></a>Syntax

BITAND(***binarynumber1** _, _ *_binarynumber2_** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _binäre Zahl1_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die erste 16-Bit-Binärzahl.  <br/> |
| _binäre Zahl2_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die zweite 16-Bit-Binärzahl.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Mit dieser Funktion können Sie in Bitmasken gespeicherte Shape-Eigenschaften testen und ändern, z. B. das Textformat des Shapes.
  
## <a name="example"></a>Beispiel

BITAND(12,6)
  
Gibt 4 zurück. 12 entspricht 0...01100. 6 entspricht 0...00110. Das Ergebnis von BITAND(12,6) lautet 0...00100.
  

