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
description: Gibt eine 16-Bit-Binärzahl in der jedes Bit auf 1 festgelegt ist, nur, wenn das entsprechende Bit in binäre Zahl 0 ist. Andernfalls wird das Bit auf 0 festgelegt.
ms.openlocfilehash: 0806e7c52cab659a09d27a60efb9c09aa436fb92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796471"
---
# <a name="bitnot-function"></a>BITNOT Function

Gibt eine 16-Bit-Binärzahl in der jedes Bit auf 1 festgelegt ist, nur, wenn das entsprechende Bit in binäre Zahl 0 ist. Andernfalls wird das Bit auf 0 festgelegt.
  
## <a name="syntax"></a>Syntax

BITNOT (** *Binärzahl* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _binäre Zahl_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Eine 16-Bit-Binärzahl.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

16-bit Binary
  
## <a name="example"></a>Beispiel

BITNOT(6)
  
Gibt 65529 zurück. Die Zahl 6 entspricht 0...00110. Daher ergibt BITNOT(6) den Wert 1...11001.
  

