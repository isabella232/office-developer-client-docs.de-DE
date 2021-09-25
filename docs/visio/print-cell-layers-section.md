---
title: Zelle "Print" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
ms.localizationpriority: medium
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: Gibt an, ob die dem Layer zugehörigen Shapes ausgedruckt werden können.
ms.openlocfilehash: 7e91daf7292da19e814a94833df40db0a75715db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608011"
---
# <a name="print-cell-layers-section"></a>Zelle "Print" (Abschnitt "Layers")

Gibt an, ob die dem Layer zugehörigen Shapes ausgedruckt werden können.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Shapes können ausgedruckt werden.  <br/> |
|FALSE  <br/> |Shapes können nicht ausgedruckt werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können diesen Wert auch über die Option **Drucken** im Dialogfeld **Layereigenschaften** festlegen. (Klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**.)
  
Um einen Verweis auf die Zelle "Print" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Layers.Print[ *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Print anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionLayer** <br/> |
|Zeilenindex:  <br/> |**visRowLayer**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visDocPreviewScope** <br/> |
   

