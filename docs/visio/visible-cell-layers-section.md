---
title: Zelle "Visible" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1110
ms.localizationpriority: medium
ms.assetid: 02048012-a814-410b-f26e-56fcfbe106e6
description: Gibt an, ob die dem Layer zugehörigen Shapes auf dem Zeichenblatt sichtbar sind.
ms.openlocfilehash: 4e5e91a0a13d2e0b6f084095da813d35316f6bc8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597723"
---
# <a name="visible-cell-layers-section"></a>Zelle "Visible" (Abschnitt "Layers")

Gibt an, ob die dem Layer zugehörigen Shapes auf dem Zeichenblatt sichtbar sind.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Shapes sind sichtbar.  <br/> |
|FALSE  <br/> |Shapes sind verborgen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Zelle entspricht der Option **"Sichtbar"** im Dialogfeld **"Layereigenschaften"** (klicken Sie auf der Registerkarte **"Start"** in **der** Bearbeitungsgruppe auf **"Layer"** und dann auf **"Layereigenschaften").** 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "Visible" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Layers.Visible[ *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Visible anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionLayer** <br/> |
|Zeilenindex:  <br/> |**visRowLayer**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visLayerVisible** <br/> |
   

