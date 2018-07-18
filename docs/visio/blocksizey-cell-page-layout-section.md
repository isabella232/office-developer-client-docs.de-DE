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
description: Bestimmt die vertikale Blockgröße, den Bereich in die jeweils auf dem Zeichenblatt passen müssen, wenn Sie Shapes mithilfe des Dialogfelds Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout, klicken Sie auf der Seite Re-Layout, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 283723bf902c07cfb044ab73107491df3c170a4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796536"
---
# <a name="blocksizey-cell-page-layout-section"></a>BlockSizeY Cell (Page Layout Section)

Bestimmt die vertikale Blockgröße, den Bereich in die jeweils auf dem Zeichenblatt passen müssen, wenn Sie Shapes mithilfe des Dialogfelds **Layout konfigurieren** (klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Re-Seitenlayout** und klicken Sie dann auf **Weitere Layoutoptionen**).
  
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, wählen Sie die Registerkarte **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)
  
Wenn Sie einen Verweis auf die Zelle BlockSizeY aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | BlockSizeY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle BlockSizeY aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOBlockSizeY** <br/> |
   

