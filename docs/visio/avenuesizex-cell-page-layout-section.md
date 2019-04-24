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
description: Legt den horizontalen Abstand zwischen den Shapes auf dem Zeichenblatt fest, wenn Sie Shapes mithilfe des Dialogfelds Layout konfigurieren (Klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu Layout, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 28eea2589e34c7793e89e01495eb519b987553a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338822"
---
# <a name="avenuesizex-cell-page-layout-section"></a>Zelle "AvenueSizeX" (Abschnitt "Page Layout")

Legt den horizontalen Abstand zwischen den Shapes auf dem Zeichenblatt fest, wenn Sie Shapes mithilfe des Dialogfelds **Layout konfigurieren** (Klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu Layout**, und klicken Sie dann auf * * mehr Layout-Optionen * *).
  
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, wählen Sie die Registerkarte **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)
  
Das dynamische Raster verwendet die Einstellung in der Zelle Zelle AvenueSizeX, wenn nur eine Form zum Berechnen des horizontalen Abstands zur Verfügung steht. Um das dynamische Raster zu verwenden, wählen Sie auf der Registerkarte **Ansicht** in der Gruppe **visuelle Hilfsmittel** die Option **dynamisches Raster**aus.
  
Wenn Sie einen Verweis auf die Zelle Zelle AvenueSizeX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle AvenueSizeY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle AvenueSizeX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOAvenueSizeX** <br/> |
   

