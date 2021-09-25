---
title: Zelle "AvenueSizeX" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm65
ms.localizationpriority: medium
ms.assetid: 86fe25ed-590d-b2f0-5dfe-9746a19c6b04
description: Bestimmt den horizontalen Abstand zwischen Shapes auf dem Zeichenblatt, wenn Sie Shapes mithilfe des Dialogfelds Layout konfigurieren anordnen (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Re-Layout Seite und dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 99bdeaee634211bbb8e300d8981b8cd66be379cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603893"
---
# <a name="avenuesizex-cell-page-layout-section"></a>Zelle "AvenueSizeX" (Abschnitt "Page Layout")

Bestimmt den horizontalen Abstand zwischen Shapes auf dem Zeichenblatt, wenn Sie Shapes mithilfe des Dialogfelds **Layout konfigurieren** anordnen (klicken Sie auf der Registerkarte **"Entwurf"** in der Gruppe **"Layout"** auf **"Seite neu anordnen",** und klicken Sie dann auf ** Weitere Layoutoptionen **).
  
## <a name="remarks"></a>HinwBemerkungeneise

Sie können diesen Wert auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, wählen Sie die Registerkarte **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)
  
Das dynamische Raster verwendet die Einstellung in der Zelle "AvenueSizeX", wenn nur eine Form für die Berechnung des horizontalen Abstands verfügbar ist. Um das dynamische Raster zu verwenden, wählen Sie auf **der** Registerkarte Ansicht in der Gruppe **Visuelle Unterstützung** **dynamisches Raster** aus.
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "AvenueSizeX" anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | AvenueSizeY  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "AvenueSizeX" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOAvenueSizeX** <br/> |
   

