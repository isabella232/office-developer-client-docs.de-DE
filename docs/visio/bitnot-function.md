---
title: BITNOT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251399
ms.localizationpriority: medium
ms.assetid: 7b6486bb-3618-3747-4b00-93bd55767c1c
description: Gibt eine 16-Bit-Binärzahl zurück, bei der jedes Bit nur auf 1 festgelegt ist, wenn das entsprechende Bit in binärer Zahl 0 ist. Andernfalls wird das Bit auf 0 festgelegt.
ms.openlocfilehash: 66a394ea9627d72e927c0b0cf4a001b4a1994dda
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554873"
---
# <a name="bitnot-function"></a>BITNOT Function

Gibt eine 16-Bit-Binärzahl zurück, bei der jedes Bit nur auf 1 festgelegt ist, wenn das entsprechende Bit in binärer Zahl 0 ist. Andernfalls wird das Bit auf 0 festgelegt.
  
## <a name="syntax"></a>Syntax

BITNOT(** *binäre Zahl* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _binäre Zahl_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Eine 16-Bit-Binärzahl.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

16-bit Binary
  
## <a name="example"></a>Beispiel

BITNOT(6)
  
Gibt 65529 zurück. Die Zahl 6 entspricht 0...00110. Daher ergibt BITNOT(6) den Wert 1...11001.
  

