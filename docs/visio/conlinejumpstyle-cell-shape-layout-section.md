---
title: Zelle "ConLineJumpStyle" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251655
localization_priority: Normal
ms.assetid: baa05a50-97d0-3769-635e-0ea20317d59a
description: Bestimmt das Liniensprungformat für Liniensprünge bei einem dynamischen Verbinder.
ms.openlocfilehash: d3e27ddb6689fb5635674b3c4a8462fe587bce7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796717"
---
# <a name="conlinejumpstyle-cell-shape-layout-section"></a>ConLineJumpStyle Cell (Shape Layout Section)

Bestimmt das Liniensprungformat für Liniensprünge bei einem dynamischen Verbinder.
  
|**Wert**|**Liniensprungformat**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Zeichenblattstandard  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |Bogen  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Lücke  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Quadrat  <br/> |**visLOJumpStyleSquare** <br/> |
|4  <br/> |Dreieck  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |3 Seiten  <br/> |**visLOJumpStyle2Point** <br/> |
|6  <br/> |4 Seiten  <br/> |**visLOJumpStyle3Point** <br/> |
|7  <br/> |5 Seiten  <br/> |**visLOJumpStyle4Point** <br/> |
|8  <br/> |6 Seiten  <br/> |**visLOJumpStyle5Point** <br/> |
|9  <br/> |7 Seiten  <br/> |**visLOJumpStyle6Point** <br/> |
   
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOJumpStyle** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können auch den Wert für diese Zelle festlegen einen dynamischen Verbinder, indem Sie in der Gruppe **Shape-Design** auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und dann auf die Registerkarte **Verbinder** . 
  
Wenn Sie einen Verweis auf die Zelle ConLineJumpStyle aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ConLineJumpStyle  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ConLineJumpStyle aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  

