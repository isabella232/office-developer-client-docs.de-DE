---
title: Zelle "Active" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm10
localization_priority: Normal
ms.assetid: 4c8e366f-9e9b-30ea-a89f-57c8d7a1168e
description: Gibt an, ob der Layer aktiv ist. Shapes ohne vorher zugewiesene Layer werden dem bzw. den aktiven Layern zugewiesen, wenn Sie sie auf das Zeichenblatt ziehen.
ms.openlocfilehash: 81d3ec083e207a927c46dda99e2b7f42c0a7bd8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796381"
---
# <a name="active-cell-layers-section"></a>Active Cell (Layers Section)

Gibt an, ob der Layer aktiv ist. Shapes ohne vorher zugewiesene Layer werden dem bzw. den aktiven Layern zugewiesen, wenn Sie sie auf das Zeichenblatt ziehen.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |
          Layer ist aktiv.
  <br/> |
|FALSE  <br/> |
          Layer ist nicht aktiv.
  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert dieser Zelle entspricht der Einstellung **Aktiv** im Dialogfeld **Layereigenschaften** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**).
  
Wenn Sie einen Verweis auf die Zelle Active aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Layers.Active [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Active aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionLayer** <br/> |
|Zeilenindex:  <br/> |**VisRowLayer** +  *i* wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visLayerActive** <br/> |
   

