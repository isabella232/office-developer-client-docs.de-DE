---
title: Zelle "BlockSizeX" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm105
localization_priority: Normal
ms.assetid: 253aac17-077e-48e0-39a8-a3abd5d4a257
description: Bestimmt die horizontale Blockgröße, den Bereich, in den jedes Ihrer Shapes auf das Zeichenblatt passen muss, wenn Sie Shapes mithilfe des Dialogfelds Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Re-Layout Seite, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 8e4cee4b2059d9b8f2fe77c2d4902e67246eac2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424189"
---
# <a name="blocksizex-cell-page-layout-section"></a>Zelle "BlockSizeX" (Abschnitt "Page Layout")

Bestimmt die horizontale Blockgröße, den Bereich, in den die einzelnen Shapes auf das Zeichenblatt passen müssen, wenn Sie Shapes mithilfe des Dialogfelds **Layout** konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe **Layout** auf **Seite** neu layout, und klicken Sie dann auf Weitere **Layoutoptionen**). 
  
## <a name="remarks"></a>Hinweise

Sie können diesen Wert auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, wählen Sie die Registerkarte **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle BlockSizeX anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |BlockSizeX  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die BlockSizeX-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOBlockSizeX** <br/> |
   

