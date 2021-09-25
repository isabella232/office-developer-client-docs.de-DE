---
title: Zelle "ShapePermeablePlace" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm885
ms.localizationpriority: medium
ms.assetid: b647cbb5-2769-068d-bbda-2dc983c47ac9
description: Legt fest, ob platzierbare Shapes über einem Shape platziert werden können, wenn Shapes unter Verwendung des Dialogfelds Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu anordnen, und klicken Sie anschließend auf Weitere Layoutoptionen) ausgerichtet werden.
ms.openlocfilehash: 384d28f742f88e6720abe497451c77cb101a3095
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607717"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a>Zelle "ShapePermeablePlace" (Abschnitt "Shape Layout")

Legt fest, ob platzierbare Shapes über einem Shape platziert werden können, wenn Shapes unter Verwendung des Dialogfelds **Layout konfigurieren** (klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu anordnen**, und klicken Sie anschließend auf **Weitere Layoutoptionen**) ausgerichtet werden.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Shapes können über einem Shape platziert werden.  <br/> |
|FALSE  <br/> |Shapes können nicht über einem Shape platziert werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können den Wert dieser Zelle auch auf der Registerkarte **Platzierung** im Dialogfeld **Verhalten** festlegen (bei ausgewähltem Shape auf der Registerkarte Entwicklertools in der Gruppe Shape-Design klicken Sie auf Verhalten und anschließend auf die Registerkarte **Platzierung).** [](run-in-developer-mode-display-the-developer-tab.md)   
  
In Versionen vor Microsoft Visio 2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt.
  
Um einen Verweis auf die Zelle ShapePermeablePlace anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapePermeablePlace  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapePermeablePlace anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOPermeablePlace** <br/> |
   

