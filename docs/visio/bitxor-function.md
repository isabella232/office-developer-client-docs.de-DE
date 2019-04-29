---
title: BITXOR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251401
localization_priority: Normal
ms.assetid: 672eacaf-a374-c7e2-b39b-8d42d2371aee
description: Gibt eine 16-Bit-Binärzahl zurück, in der jedes Bit auf 1 festgelegt ist, wenn das entsprechende Bit in beiden, aber nicht binären number1 und binären number2 1 ist. Andernfalls ist das Bit auf 0 festgelegt.
ms.openlocfilehash: ab8ff46fe98512d963ef4ecd5c37127353827725
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439233"
---
# <a name="bitxor-function"></a>BITXOR Function

Gibt eine 16-Bit-Binärzahl zurück, in der jedes Bit auf 1 festgelegt ist, wenn das entsprechende Bit in beiden, aber nicht binären number1 und binären number2 1 ist. Andernfalls ist das Bit auf 0 festgelegt.
  
## <a name="syntax"></a>Syntax

BITXOR (* * *Binary number1* * *, * * *Binary number2* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _binäre number1_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die erste 16-Bit-Binärzahl.  <br/> |
| _binäre number2_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die zweite 16-Bit-Binärzahl.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

16-bit Binary
  
## <a name="example"></a>Beispiel

BITXOR (12, 6)
  
Gibt 10 zurück. Die Zahl 12 entspricht 0...01100. Die Zahl 6 entspricht 0...00110. Daher ergibt BITXOR(12,6) den Wert 0...0,01010.
  

