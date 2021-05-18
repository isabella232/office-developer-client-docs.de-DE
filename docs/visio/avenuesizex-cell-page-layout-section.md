---
title: Zelle "AvenueSizeX" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm65
localization_priority: Normal
ms.assetid: 86fe25ed-590d-b2f0-5dfe-9746a19c6b04
description: Bestimmt den horizontalen Abstand zwischen Shapes auf dem Zeichenblatt, wenn Sie Shapes mithilfe des Dialogfelds Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Re-Layout Seite, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 28eea2589e34c7793e89e01495eb519b987553a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411645"
---
# <a name="avenuesizex-cell-page-layout-section"></a>Zelle "AvenueSizeX" (Abschnitt "Page Layout")

Bestimmt den horizontalen Abstand zwischen Shapes auf dem Zeichenblatt, wenn Sie Shapes  mithilfe des Dialogfelds Layout konfigurieren (klicken Sie auf der Registerkarte **Entwurf** in der Gruppe Layout auf **Seite** neu layout, und klicken Sie dann auf ** Weitere Layoutoptionen **). 
  
## <a name="remarks"></a>Hinweise

Sie können diesen Wert auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, wählen Sie die Registerkarte **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)
  
Das dynamische Raster verwendet die Einstellung in der Zelle AvenueSizeX, wenn nur eine Form zum Berechnen des horizontalen Abstands verfügbar ist. Um das dynamische Raster zu verwenden, wählen Sie auf **der** Registerkarte Ansicht in der **Gruppe Visuelle** Hilfen **dynamisches Raster aus.**
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle AvenueSizeX anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | AvenueSizeY  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die AvenueSizeX-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOAvenueSizeX** <br/> |
   

