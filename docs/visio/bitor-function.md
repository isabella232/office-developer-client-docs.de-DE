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
description: Gibt eine 16-Bit-Binärzahl zurück, in der jedes Bit auf 1 festgelegt ist, wenn das entsprechende Bit in binary number1 oder Binary number2 1 ist. Das Bit wird nur dann auf 0 festgelegt, wenn das entsprechende Bit sowohl in binären number1 als auch in binären number2 0 ist.
ms.openlocfilehash: 13bda2c6c65557b1f8372432cf919b2aaf2d75de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303374"
---
# <a name="bitor-function"></a>BITOR Function

Gibt eine 16-Bit-Binärzahl zurück, in der jedes Bit auf 1 festgelegt ist, wenn das entsprechende Bit in *Binary number1* oder *Binary number2* 1 ist. Das Bit wird nur dann auf 0 festgelegt, wenn das entsprechende Bit sowohl in *binären number1* als auch in *binären number2* 0 ist. 
  
## <a name="syntax"></a>Syntax

BITOR (* * *Binary number1* * *, * * *Binary number2* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _binäre number1_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Die erste 16-Bit-Binärzahl.  <br/> |
| _binäre number2_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Die zweite 16-Bit-Binärzahl.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

16-bit Binary
  
## <a name="example"></a>Beispiel

BITOR (12, 6)
  
Gibt 14 zurück. Die Zahl 12 entspricht 0...01100. Die Zahl 6 entspricht 0...00110. Daher ergibt BITOR(12,6) den Wert 0...01110.
  

