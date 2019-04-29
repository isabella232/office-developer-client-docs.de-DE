---
title: Zelle "Snap" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251355
localization_priority: Normal
ms.assetid: c1b24e45-6f08-686b-b53d-e85fb9087a50
description: Bestimmt, ob andere Shapes an den dem Layer zugeordneten Shapes einrasten können. Die dem Layer zugeordneten Shapes können an anderen Shapes einrasten, andere Shapes jedoch nicht.
ms.openlocfilehash: 87e7e7500469fb7f8c7fdd4771a0225d0e4fc993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434844"
---
# <a name="snap-cell-layers-section"></a>Zelle "Snap" (Abschnitt "Layers")

Bestimmt, ob andere Shapes an den dem Layer zugeordneten Shapes einrasten können. Die dem Layer zugeordneten Shapes können an anderen Shapes einrasten, andere Shapes jedoch nicht.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Andere Shapes können an den dem Layer zugeordneten Shapes einrasten.  <br/> |
|FALSE  <br/> |Andere Shapes können an den dem Layer zugeordneten Shapes nicht einrasten.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch über die Option **Ausrichten** im Dialogfeld **Layereigenschaften** festlegen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**).
  
Wenn Sie einen Verweis auf die Zelle "Snap" aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Layers. Snap [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "Snap" aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionLayer** <br/> |
|Zeilenindex:  <br/> |**visRowLayer** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visLayerSnap** <br/> |
   

