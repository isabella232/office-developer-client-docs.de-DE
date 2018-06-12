---
title: Zelle "Width" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251194
localization_priority: Normal
ms.assetid: 992ae9d8-ea15-0f5c-ccd6-e4c536099692
description: 'Enthält die Breite des ausgewählten Shapes in Zeichnungseinheiten. Die Standardformel zur Bestimmung der Breite eines 1D-Shapes lautet:'
ms.openlocfilehash: 55e77c5ccfca2425a8a2985564448e0f656aebbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798409"
---
# <a name="width-cell-shape-transform-section"></a>Width Cell (Shape Transform Section)

Enthält die Breite des ausgewählten Shapes in Zeichnungseinheiten. Die Standardformel zur Bestimmung der Breite eines 1D-Shapes lautet:
  
= SQRT((EndeX - AnfangX) ^ 2 + (EndeY - AnfangY) ^ 2)
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle Width nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Width  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Width aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
| Zellenindex:  <br/> |**visXFormWidth** <br/> |
   

