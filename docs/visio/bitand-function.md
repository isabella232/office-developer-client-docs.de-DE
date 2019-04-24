---
title: BITAND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251398
localization_priority: Normal
ms.assetid: c437de23-d2e0-469d-62e6-8eb8b8cfea5c
description: Gibt eine 16-Bit-Binärzahl zurück, in der jedes Bit nur dann auf 1 festgelegt ist, wenn das entsprechende Bit in binarynumber1 und binarynumber2 1 ist. Andernfalls ist das Bit auf 0 festgelegt.
ms.openlocfilehash: 495ad645a422c0333d02a22c3c600dd1e0d567bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284469"
---
# <a name="bitand-function"></a>BITAND Function

Gibt eine 16-Bit-Binärzahl zurück, in der jedes Bit nur dann auf 1 festgelegt ist, wenn das entsprechende Bit in binarynumber1 und binarynumber2 1 ist. Andernfalls ist das Bit auf 0 festgelegt. 
  
## <a name="syntax"></a>Syntax

BITUND (* * *binarynumber1* * *, * * *binarynumber2* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _binäre number1_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Die erste 16-Bit-Binärzahl.  <br/> |
| _binäre number2_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Die zweite 16-Bit-Binärzahl.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Mit dieser Funktion können Sie in Bitmasken gespeicherte Shape-Eigenschaften testen und ändern, z. B. das Textformat des Shapes.
  
## <a name="example"></a>Beispiel

BITUND (12, 6)
  
Gibt 4 zurück. 12 entspricht 0...01100. 6 entspricht 0...00110. Das Ergebnis von BITAND(12,6) lautet 0...00100.
  

