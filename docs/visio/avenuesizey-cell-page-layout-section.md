---
title: Zelle "AvenueSizeY" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm70
ms.localizationpriority: medium
ms.assetid: 9ff2893c-afe5-505e-0b55-48ec1de08a5f
description: Bestimmt den vertikalen Abstand zwischen Shapes auf dem Zeichenblatt, wenn Sie Shapes mithilfe des Dialogfelds Layout konfigurieren anordnen (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Re-Layout Seite und anschließend auf Weitere Layoutoptionen).
ms.openlocfilehash: 08c40814735f4e2db8092221c99f9213857f14ec
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578186"
---
# <a name="avenuesizey-cell-page-layout-section"></a>Zelle "AvenueSizeY" (Abschnitt "Page Layout")

Bestimmt den vertikalen Abstand zwischen Shapes auf dem Zeichenblatt, wenn Sie Shapes mithilfe des Dialogfelds **Layout konfigurieren** anordnen (klicken Sie auf der Registerkarte Entwurf in der Gruppe **Layout** auf Seite neu  anordnen und anschließend auf **Weitere Layoutoptionen).** 
  
## <a name="remarks"></a>HinwBemerkungeneise

Sie können diesen Wert auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, wählen Sie die Registerkarte **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)
  
Das dynamische Raster verwendet die Einstellung in der Zelle "AvenueSizeY", wenn nur eine Form für die Berechnung des vertikalen Abstands verfügbar ist. Um das dynamische Raster zu verwenden, wählen Sie auf **der** Registerkarte Ansicht in der Gruppe **Visuelle Unterstützung** **dynamisches Raster** aus.
  
Verwenden Sie zum Abrufen eines Verweises auf die Zelle "AvenueSizeY" anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | AvenueSizeY  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "AvenueSizeY" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOAvenueSizeY** <br/> |
   

