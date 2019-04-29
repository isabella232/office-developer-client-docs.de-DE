---
title: Zelle "Visible" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1110
localization_priority: Normal
ms.assetid: 02048012-a814-410b-f26e-56fcfbe106e6
description: Gibt an, ob die dem Layer zugehörigen Shapes auf dem Zeichenblatt sichtbar sind.
ms.openlocfilehash: 4266debc318c839bdd29fa818d11b5e1da669a9e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405450"
---
# <a name="visible-cell-layers-section"></a>Zelle "Visible" (Abschnitt "Layers")

Gibt an, ob die dem Layer zugehörigen Shapes auf dem Zeichenblatt sichtbar sind.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Shapes sind sichtbar.  <br/> |
|FALSE  <br/> |Shapes sind verborgen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Zelle entspricht der Option **Visible** im Dialogfeld **Layereigenschaften** (Klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften** ). 
  
Wenn Sie einen Verweis auf die Zelle Visible aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Layers. Visible [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Visible aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionLayer** <br/> |
|Zeilenindex:  <br/> |**visRowLayer** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visLayerVisible** <br/> |
   

