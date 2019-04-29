---
title: Zelle "BlockSizeY" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm110
localization_priority: Normal
ms.assetid: be51e18e-ea49-0788-1a17-866090afb9f4
description: Bestimmt die vertikale Blockgröße, den Bereich, in dem jede Ihrer Shapes auf das Zeichenblatt passen muss, wenn Sie Shapes mithilfe des Dialogfelds Layout konfigurieren (Klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu Layout, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 08f2012bb027267810c21ef253a0073bb42d3a96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427402"
---
# <a name="blocksizey-cell-page-layout-section"></a>Zelle "BlockSizeY" (Abschnitt "Page Layout")

Bestimmt die vertikale Blockgröße, den Bereich, in dem jede Ihrer Shapes auf das Zeichenblatt passen muss, wenn Sie Shapes mithilfe des Dialogfelds **Layout konfigurieren** (Klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu Layout**). und klicken Sie dann auf **Weitere Layoutoptionen**).
  
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, wählen Sie die Registerkarte **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)
  
Wenn Sie einen Verweis auf die Zelle Zelle BlockSizeY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle BlockSizeY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle BlockSizeY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOBlockSizeY** <br/> |
   

