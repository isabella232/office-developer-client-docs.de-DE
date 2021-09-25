---
title: Zelle "ShapePermeableX" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm890
ms.localizationpriority: medium
ms.assetid: 7e27b36c-4fd1-34e0-c168-f49eb5757b0e
description: Legt fest, ob ein Verbinder horizontal durch ein platzierbares Shape geleitet werden kann.
ms.openlocfilehash: 38245e7ce35943b9973853b58c54200a5d856d67
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607689"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a>Zelle "ShapePermeableX" (Abschnitt "Shape Layout")

Legt fest, ob ein Verbinder horizontal durch ein platzierbares Shape geleitet werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Verbinder können horizontal durch ein platzierbares Shape geleitet werden.  <br/> |
|FALSE  <br/> |Verbinder können nicht horizontal durch ein platzierbares Shape geleitet werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können den Wert dieser Zelle auch auf der Registerkarte **Platzierung** im Dialogfeld **Verhalten** festlegen (bei ausgewähltem Shape auf der Registerkarte Entwicklertools in der Gruppe Shape-Design klicken Sie auf Verhalten und anschließend auf die Registerkarte **Platzierung).** [](run-in-developer-mode-display-the-developer-tab.md)   
  
In Versionen vor Visio 2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt. 
  
Um einen Verweis auf die Zelle "ShapePermeableX" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapePermeableX  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapePermeableX anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOPermX** <br/> |
   

