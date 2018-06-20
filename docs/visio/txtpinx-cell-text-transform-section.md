---
title: Zelle "TxtPinX" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Legt die X--Koordinate des Textblocks des Drehung im Verhältnis zum Ursprung des Shapes. Die Standardformel lautet:'
ms.openlocfilehash: df103557d103dbde7e4a1c8d67cabe37a0af9311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798324"
---
# <a name="txtpinx-cell-text-transform-section"></a>Zelle "TxtPinX" (Abschnitt "Text Transform")

Legt die *X* --Koordinate des Textblocks des Drehung im Verhältnis zum Ursprung des Shapes. Die Standardformel lautet: 
  
= Breite \* 0,5
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle TxtPinX nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TxtPinX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle TxtPinX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowTextXForm** <br/> |
| Zellenindex:  <br/> |**visXFormPinX** <br/> |
   

