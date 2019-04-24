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
ms.openlocfilehash: c99f4669f3b27390a5b8e9062d6085a5a9db54e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351219"
---
# <a name="width-cell-shape-transform-section"></a>Zelle "Width" (Abschnitt "Shape Transform")

Enthält die Breite des ausgewählten Shapes in Zeichnungseinheiten. Die Standardformel zur Bestimmung der Breite eines 1D-Shapes lautet:
  
= SQRT((EndeX - AnfangX) ^ 2 + (EndeY - AnfangY) ^ 2)
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Width aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Width  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "width" aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
| Zellenindex:  <br/> |**visXFormWidth** <br/> |
   

