---
title: Zelle "ShapePermeableX" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm890
localization_priority: Normal
ms.assetid: 7e27b36c-4fd1-34e0-c168-f49eb5757b0e
description: Legt fest, ob ein Verbinder horizontal durch ein platzierbares Shape geleitet werden kann.
ms.openlocfilehash: 21fa1683c4b1afd24992ec7a8a6daa52a8280825
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409475"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a>Zelle "ShapePermeableX" (Abschnitt "Shape Layout")

Legt fest, ob ein Verbinder horizontal durch ein platzierbares Shape geleitet werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Verbinder können horizontal durch ein platzierbares Shape geleitet werden.  <br/> |
|FALSE  <br/> |Verbinder können nicht horizontal durch ein platzierbares Shape geleitet werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können den Wert dieser Zelle auch auf der Registerkarte Platzierung im Dialogfeld [](run-in-developer-mode-display-the-developer-tab.md) Verhalten festlegen (wenn eine Form ausgewählt ist, klicken  Sie auf der Registerkarte Entwickler in der Gruppe **Shape-Entwurf** auf **Verhalten,** und klicken Sie dann auf die Registerkarte Platzierung).   
  
In Versionen vor Visio 2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt. 
  
Um einen Verweis auf die Zelle ShapePermeableX anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapePermeableX  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ShapePermeableX-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOPermX** <br/> |
   

