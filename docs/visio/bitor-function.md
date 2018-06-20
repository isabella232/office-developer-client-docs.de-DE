---
title: BITOR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251400
localization_priority: Normal
ms.assetid: 1d0954c5-b2cb-6c5d-62b3-a68011cf0c85
description: Gibt eine 16-Bit-Binärzahl in der jedes Bit auf 1 festgelegt ist, wenn das entsprechende Bit in binary number1 oder binary number2 1 ist. Nur, wenn das entsprechende Bit in binary Zahl1 und binäre Zahl2 0 ist, wird das Bit auf 0 festgelegt.
ms.openlocfilehash: db9808f16b32776149abbddf882310c02268cec3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796488"
---
# <a name="bitor-function"></a>BITOR Function

Gibt eine 16-Bit-Binärzahl in der jedes Bit auf 1 festgelegt ist, wenn das entsprechende Bit in *binary number1* oder *binary Zahl2* 1 ist. Nur, wenn das entsprechende Bit in *binary Zahl1* und *binäre Zahl2* 0 ist, wird das Bit auf 0 festgelegt. 
  
## <a name="syntax"></a>Syntax

BITOR (** *binary Zahl1* **, ** *binary Zahl2* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _binäre Zahl1_ <br/> |Erforderlich  <br/> |**Numerische** <br/> |Die erste 16-Bit-Binärzahl.  <br/> |
| _binäre Zahl2_ <br/> |Erforderlich  <br/> |**Numerische** <br/> |Die zweite 16-Bit-Binärzahl.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

16-bit Binary
  
## <a name="example"></a>Beispiel

BITOR(12,6)
  
Gibt 14 zurück. Die Zahl 12 entspricht 0...01100. Die Zahl 6 entspricht 0...00110. Daher ergibt BITOR(12,6) den Wert 0...01110.
  

