---
title: BITNOT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251399
localization_priority: Normal
ms.assetid: 7b6486bb-3618-3747-4b00-93bd55767c1c
description: Gibt eine 16-Bit-Binärzahl zurück, in der jedes Bit nur dann auf 1 festgelegt ist, wenn das entsprechende Bit in binary number 0 ist. Andernfalls ist das Bit auf 0 festgelegt.
ms.openlocfilehash: 34ea6fd614feae8e3c8e97e34b7ff6c531f4c123
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330009"
---
# <a name="bitnot-function"></a>BITNOT Function

Gibt eine 16-Bit-Binärzahl zurück, in der jedes Bit nur dann auf 1 festgelegt ist, wenn das entsprechende Bit in binary number 0 ist. Andernfalls ist das Bit auf 0 festgelegt.
  
## <a name="syntax"></a>Syntax

BITNOT (* * *Binärzahl* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _binäre Zahl_ <br/> |Erforderlich  <br/> |**Numerisch** <br/> |Eine 16-Bit-Binärzahl.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

16-bit Binary
  
## <a name="example"></a>Beispiel

BITNOT (6)
  
Gibt 65529 zurück. Die Zahl 6 entspricht 0...00110. Daher ergibt BITNOT(6) den Wert 1...11001.
  

