---
title: BITXOR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251401
ms.localizationpriority: medium
ms.assetid: 672eacaf-a374-c7e2-b39b-8d42d2371aee
description: Gibt eine 16-Bit-Binärzahl zurück, bei der jedes Bit auf 1 festgelegt ist, wenn das entsprechende Bit in der binären Zahl1 und der binären Zahl2 1 ist. Andernfalls wird das Bit auf 0 festgelegt.
ms.openlocfilehash: b374eff1fb2644124bb5b4f2a52021d91b00df72
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616012"
---
# <a name="bitxor-function"></a>BITXOR Function

Gibt eine 16-Bit-Binärzahl zurück, bei der jedes Bit auf 1 festgelegt ist, wenn das entsprechende Bit in der binären Zahl1 und der binären Zahl2 1 ist. Andernfalls wird das Bit auf 0 festgelegt.
  
## <a name="syntax"></a>Syntax

BITXOR(** *binary number1* **, ** *binary number2* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _binäre Zahl1_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die erste 16-Bit-Binärzahl.  <br/> |
| _binäre Zahl2_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die zweite 16-Bit-Binärzahl.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

16-bit Binary
  
## <a name="example"></a>Beispiel

BITXOR(12,6)
  
Gibt 10 zurück. Die Zahl 12 entspricht 0...01100. Die Zahl 6 entspricht 0...00110. Daher ergibt BITXOR(12,6) den Wert 0...0,01010.
  

