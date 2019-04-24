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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357050"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a>Zelle "ShapePermeableX" (Abschnitt "Shape Layout")

Legt fest, ob ein Verbinder horizontal durch ein platzierbares Shape geleitet werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Verbinder können horizontal durch ein platzierbares Shape geleitet werden.  <br/> |
|FALSE  <br/> |Verbinder können nicht horizontal durch ein platzierbares Shape geleitet werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch im Dialogfeld **Verhalten** auf der Registerkarte **Platzierung** festlegen (wenn ein Shape ausgewählt ist, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten**, und klicken Sie dann auf die Registerkarte **Platzierung** ). 
  
In Versionen vor Visio 2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt. 
  
Wenn Sie einen Verweis auf die Zelle Zelle ShapePermeableX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle ShapePermeableX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ShapePermeableX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOPermX** <br/> |
   

