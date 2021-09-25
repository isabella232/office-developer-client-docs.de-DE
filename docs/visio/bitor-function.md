---
title: BITOR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251400
ms.localizationpriority: medium
ms.assetid: 1d0954c5-b2cb-6c5d-62b3-a68011cf0c85
description: Gibt eine 16-Bit-Binärzahl zurück, bei der jedes Bit auf 1 festgelegt ist, wenn das entsprechende Bit in binärer Zahl1 oder binärer Zahl2 1 ist. Das Bit wird nur auf 0 festgelegt, wenn das entsprechende Bit in binärer Zahl1 und binärer Zahl2 0 ist.
ms.openlocfilehash: 6f6e6176e2e14291547db31514fd105622a44fd4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616019"
---
# <a name="bitor-function"></a>BITOR Function

Gibt eine 16-Bit-Binärzahl zurück, bei der jedes Bit auf 1 festgelegt ist, wenn das entsprechende Bit in  *binärer Zahl1*  oder  *binärer Zahl2*  1 ist. Das Bit wird nur auf 0 festgelegt, wenn das entsprechende Bit in  *binärer Zahl1*  und  *binärer Zahl2*  0 ist. 
  
## <a name="syntax"></a>Syntax

BITOR(** *binary number1* **, ** *binary number2* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _binäre Zahl1_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die erste 16-Bit-Binärzahl.  <br/> |
| _binäre Zahl2_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Die zweite 16-Bit-Binärzahl.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

16-bit Binary
  
## <a name="example"></a>Beispiel

BITOR(12,6)
  
Gibt 14 zurück. Die Zahl 12 entspricht 0...01100. Die Zahl 6 entspricht 0...00110. Daher ergibt BITOR(12,6) den Wert 0...01110.
  

