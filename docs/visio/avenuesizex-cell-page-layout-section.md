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
description: Bestimmt den horizontalen Abstand zwischen Shapes auf dem Zeichenblatt, wenn Sie Shapes mithilfe des Dialogfelds Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout, klicken Sie auf der Seite Re-Layout, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: efb29181414957063e038b97c2d7b79720aa0405
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796429"
---
# <a name="avenuesizex-cell-page-layout-section"></a>AvenueSizeX Cell (Page Layout Section)

Bestimmt den horizontalen Abstand zwischen Shapes auf dem Zeichenblatt, wenn Sie Shapes mithilfe des Dialogfelds **Layout konfigurieren** (auf der Registerkarte **Entwurf** in der Gruppe **Layout** , klicken Sie auf **Der Seite Re-Layout**, und klicken Sie dann auf ** mehr Layoutoptionen **).
  
## <a name="remarks"></a>Hinweise

Sie können diesen Wert auch im Dialogfeld **Layout und Routing Abstand** festlegen (klicken Sie auf der Registerkarte **Entwurf** klicken Sie auf den Pfeil in der Gruppe **Seite einrichten** , klicken Sie auf der Registerkarte **Layout und Routing** und klicken Sie dann auf **Abstand**).
  
Das dynamische Gitter verwendet die Einstellung in der Zelle AvenueSizeX, wenn nur eine Form zur Berechnung der horizontalen Abstands verfügbar ist. Wählen Sie das dynamische Raster wählen Sie auf der Registerkarte **Ansicht** in der Gruppe **visuelle Hilfsmittel** verwenden, um **Dynamische Gitter**aus.
  
Zum Abrufen eines Verweises auf die Zelle AvenueSizeX nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | AvenueSizeY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle AvenueSizeX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOAvenueSizeX** <br/> |
   

