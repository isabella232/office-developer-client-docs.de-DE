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
ms.openlocfilehash: f97f7dc09d1f882452ae2234882de45f06bd0da1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338780"
---
# <a name="active-cell-layers-section"></a>Zelle "Active" (Abschnitt "Layers")

Gibt an, ob der Layer aktiv ist. Shapes ohne vorher zugewiesene Layer werden dem bzw. den aktiven Layern zugewiesen, wenn Sie sie auf das Zeichenblatt ziehen.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Layer ist aktiv.  <br/> |
|FALSE  <br/> |Layer ist nicht aktiv.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert dieser Zelle entspricht der Einstellung **Aktiv** im Dialogfeld **Layereigenschaften** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**).
  
Wenn Sie einen Verweis auf die aktive Zelle aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Layers. Active [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die aktive Zelle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionLayer** <br/> |
|Zeilenindex:  <br/> |**visRowLayer** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visLayerActive** <br/> |
   

