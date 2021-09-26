---
title: Zelle "Glue" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
ms.localizationpriority: medium
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: Gibt an, ob die dem Layer zugehörigen Shapes geklebt werden können.
ms.openlocfilehash: 64935dfd8964757f3b8590519fbb0c883200e178
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612778"
---
# <a name="glue-cell-layers-section"></a>Zelle "Glue" (Abschnitt "Layers")

Gibt an, ob die dem Layer zugehörigen Shapes geklebt werden können.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Klebefunktion ist aktiviert.  <br/> |
|FALSE  <br/> |Klebefunktion ist deaktiviert.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Zelle entspricht der Option **"Kleben"** im Dialogfeld **"Layereigenschaften"** (klicken Sie auf der Registerkarte **"Start"** in der Gruppe **"Bearbeiten"** auf **"Layer"** und dann auf **"Layereigenschaften").** 
  
Um einen Verweis auf die Zelle "Glue" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Layers.Glue[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Um einen Verweis auf die Zelle "Glue" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionLayer** <br/> |
|Zeilenindex:  <br/> |**visRowLayer**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visLayerGlue** <br/> |
   

