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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438834"
---
# <a name="bitnot-function"></a>BITNOT Function

Gibt eine 16-Bit-Binärzahl zurück, in der jedes Bit nur dann auf 1 festgelegt ist, wenn das entsprechende Bit in binary number 0 ist. Andernfalls ist das Bit auf 0 festgelegt.
  
## <a name="syntax"></a>Syntax

BITNOT (* * *Binärzahl* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _binäre Zahl_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Eine 16-Bit-Binärzahl.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

16-bit Binary
  
## <a name="example"></a>Beispiel

BITNOT (6)
  
Gibt 65529 zurück. Die Zahl 6 entspricht 0...00110. Daher ergibt BITNOT(6) den Wert 1...11001.
  

