---
title: Zelle "Print" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
localization_priority: Normal
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: Gibt an, ob die dem Layer zugehörigen Shapes ausgedruckt werden können.
ms.openlocfilehash: f9a1dca6d45b53c02ff0ed29f921c352fc947630
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435215"
---
# <a name="print-cell-layers-section"></a>Zelle "Print" (Abschnitt "Layers")

Gibt an, ob die dem Layer zugehörigen Shapes ausgedruckt werden können.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Shapes können ausgedruckt werden.  <br/> |
|FALSE  <br/> |Shapes können nicht ausgedruckt werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können diesen Wert auch über die Option **Drucken** im Dialogfeld **Layereigenschaften** festlegen. (Klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**.)
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle Print anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Layers.Print[ *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Print nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionLayer** <br/> |
|Zeilenindex:  <br/> |**visRowLayer**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visDocPreviewScope** <br/> |
   

