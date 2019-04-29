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
description: 'Bestimmt die x-Koordinate des Drehmittelpunkts des Textblocks im Verhältnis zum Ursprung der Form. Die Standardformel lautet:'
ms.openlocfilehash: 836f5c807d0c0e53efc825f62f60429274282165
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423496"
---
# <a name="txtpinx-cell-text-transform-section"></a>Zelle "TxtPinX" (Abschnitt "Text Transform")

Bestimmt die *x* -Koordinate des Drehmittelpunkts des Textblocks im Verhältnis zum Ursprung der Form. Die Standardformel lautet: 
  
= Breite \* 0,5
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle TxtPinX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle TxtPinX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle TxtPinX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowTextXForm** <br/> |
| Zellenindex:  <br/> |**visXFormPinX** <br/> |
   

