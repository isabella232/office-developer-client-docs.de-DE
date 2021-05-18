---
title: Zelle "Glue" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
localization_priority: Normal
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: Gibt an, ob die dem Layer zugehörigen Shapes geklebt werden können.
ms.openlocfilehash: 55886a7e96bd2c08966cb85f5edad6a7174e30cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408516"
---
# <a name="glue-cell-layers-section"></a>Zelle "Glue" (Abschnitt "Layers")

Gibt an, ob die dem Layer zugehörigen Shapes geklebt werden können.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Klebefunktion ist aktiviert.  <br/> |
|FALSE  <br/> |Klebefunktion ist deaktiviert.  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Zelle entspricht der Option  **Kleben** im Dialogfeld Layereigenschaften (klicken Sie auf der Registerkarte **Start** in der Gruppe Bearbeiten auf **Ebenen,** und klicken Sie dann auf **Layereigenschaften** ).  
  
Um einen Verweis auf die Zelle Glue anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Layers.Glue[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Glue nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionLayer** <br/> |
|Zeilenindex:  <br/> |**visRowLayer**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visLayerGlue** <br/> |
   

