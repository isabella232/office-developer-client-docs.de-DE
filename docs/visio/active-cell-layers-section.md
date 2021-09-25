---
title: Zelle "Active" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm10
ms.localizationpriority: medium
ms.assetid: 4c8e366f-9e9b-30ea-a89f-57c8d7a1168e
description: Gibt an, ob der Layer aktiv ist. Shapes ohne vorher zugewiesene Layer werden dem bzw. den aktiven Layern zugewiesen, wenn Sie sie auf das Zeichenblatt ziehen.
ms.openlocfilehash: bf300a911084cdd05e270bb3e960934d9a4e0e4e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616047"
---
# <a name="active-cell-layers-section"></a>Zelle "Active" (Abschnitt "Layers")

Gibt an, ob der Layer aktiv ist. Shapes ohne vorher zugewiesene Layer werden dem bzw. den aktiven Layern zugewiesen, wenn Sie sie auf das Zeichenblatt ziehen.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Layer ist aktiv.  <br/> |
|FALSE  <br/> |Layer ist nicht aktiv.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert dieser Zelle entspricht der Einstellung **Aktiv** im Dialogfeld **Layereigenschaften** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**).
  
Um einen Verweis auf die aktive Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Layers.Active[ *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Um einen Verweis auf die aktive Zelle anhand des Indexes aus einem Programm abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionLayer** <br/> |
|Zeilenindex:  <br/> |**visRowLayer**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visLayerActive** <br/> |
   

