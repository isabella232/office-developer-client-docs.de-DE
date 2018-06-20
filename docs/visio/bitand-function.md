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
description: Gibt eine 16-Bit-Binärzahl in der jedes Bit auf 1 festgelegt ist, nur, wenn das entsprechende Bit in Binärzahl1 und binarynumber2 1 ist. Andernfalls wird das Bit auf 0 festgelegt.
ms.openlocfilehash: 0b501bb383596e3f2f39ea14f2cb9eb4bf40b25b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796496"
---
# <a name="bitand-function"></a>BITAND-Funktion

Gibt eine 16-Bit-Binärzahl in der jedes Bit auf 1 festgelegt ist, nur, wenn das entsprechende Bit in Binärzahl1 und binarynumber2 1 ist. Andernfalls wird das Bit auf 0 festgelegt. 
  
## <a name="syntax"></a>Syntax

BITAND (** *Binärzahl1* **, ** *binarynumber2* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _binäre Zahl1_ <br/> |Erforderlich  <br/> |**Numerische** <br/> |Die erste 16-Bit-Binärzahl.  <br/> |
| _binäre Zahl2_ <br/> |Erforderlich  <br/> |**Numerische** <br/> |Die zweite 16-Bit-Binärzahl.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Mit dieser Funktion können Sie in Bitmasken gespeicherte Shape-Eigenschaften testen und ändern, z. B. das Textformat des Shapes.
  
## <a name="example"></a>Beispiel

BITAND(12,6)
  
Gibt 4 zurück. 12 entspricht 0...01100. 6 entspricht 0...00110. Das Ergebnis von BITAND(12,6) lautet 0...00100.
  

