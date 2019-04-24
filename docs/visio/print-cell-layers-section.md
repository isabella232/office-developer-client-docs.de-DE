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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356182"
---
# <a name="print-cell-layers-section"></a>Zelle "Print" (Abschnitt "Layers")

Gibt an, ob die dem Layer zugehörigen Shapes ausgedruckt werden können.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Shapes können ausgedruckt werden.  <br/> |
|FALSE  <br/> |Shapes können nicht ausgedruckt werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch über die Option **Drucken** im Dialogfeld **Layereigenschaften** festlegen. (Klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**.)
  
Wenn Sie einen Verweis auf die Zelle "Print" aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Layers. print [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "Print" aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionLayer** <br/> |
|Zeilenindex:  <br/> |**visRowLayer** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visDocPreviewScope** <br/> |
   

