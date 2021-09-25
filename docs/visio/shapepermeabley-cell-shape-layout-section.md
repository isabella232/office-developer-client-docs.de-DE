---
title: Zelle "ShapePermeableY" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251666
ms.localizationpriority: medium
ms.assetid: 90701ecf-3d34-2eac-9ee9-7965e16c0f7c
description: Legt fest, ob ein Verbinder vertikal durch ein Shape geleitet werden kann.
ms.openlocfilehash: c4625eadf2d9729c08204eac6d6d12b9b7f69408
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573355"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a>Zelle "ShapePermeableY" (Abschnitt "Shape Layout")

Legt fest, ob ein Verbinder vertikal durch ein Shape geleitet werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Verbinder können vertikal durch ein Shape geleitet werden.  <br/> |
|FALSE  <br/> |Verbinder können nicht vertikal durch ein Shape geleitet werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können den Wert dieser Zelle auch auf der Registerkarte **Platzierung** im Dialogfeld **Verhalten** festlegen (bei ausgewähltem Shape auf der Registerkarte Entwicklertools in der Gruppe Shape-Design klicken Sie auf Verhalten und anschließend auf die Registerkarte **Platzierung).** [](run-in-developer-mode-display-the-developer-tab.md)   
  
In Versionen vor Visio 2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt.
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle ShapePermeableY anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapePermeableY  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapePermeableY anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOPermY** <br/> |
   

