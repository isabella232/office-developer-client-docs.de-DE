---
title: Zelle "ShapePlaceStyle" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70007
ms.localizationpriority: medium
ms.assetid: 29bfe8ec-ca12-8fbf-b62b-ece3710dfe2e
description: Gibt an, wie Shapes auf dem Zeichenblatt platziert werden, wenn Shapes im Dialogfeld Layout konfigurieren angeordnet werden (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Re-Layout Seite und dann auf Weitere Layoutoptionen). Speichert Layoutstil- und Ausrichtungswerte aus VisCellIndices.
ms.openlocfilehash: e3347c25559191c5605dd70d8461680e1134d3bd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549623"
---
# <a name="shapeplacestyle-cell-shape-layout-section"></a>Zelle "ShapePlaceStyle" (Abschnitt "Shape Layout")

Gibt an, wie Shapes auf dem Zeichenblatt platziert werden, wenn Shapes im Dialogfeld **Layout konfigurieren** angeordnet werden (klicken Sie auf der Registerkarte **"Entwurf"** in der Gruppe **"Layout"** auf **"Seite neu anordnen"** und dann auf **"Weitere Layoutoptionen").** Speichert Layoutstil- und Ausrichtungswerte aus **VisCellIndices**. 
  
|**Konstante**|**Wert**|
|:-----|:-----|
|**visLOPlaceBottomToTop** <br/> |4   <br/> |
|**visLOPlaceCircular** <br/> |6   <br/> |
|**visLOPlaceCompactDownLeft** <br/> |14   <br/> |
|**visLOPlaceCompactDownRight** <br/> |7   <br/> |
|**visLOPlaceCompactLeftDown** <br/> |13  <br/> |
|**visLOPlaceCompactLeftUp** <br/> |12   <br/> |
|**visLOPlaceCompactRightDown** <br/> |8   <br/> |
|**visLOPlaceCompactRightUp** <br/> |9   <br/> |
|**visLOPlaceCompactUpLeft** <br/> |11  <br/> |
|**visLOPlaceCompactUpRight** <br/> |10  <br/> |
|**visLOPlaceDefault** <br/> |0  <br/> |
|**visLOPlaceHierarchyBottomToTopCenter** <br/> |20  <br/> |
|**visLOPlaceHierarchyBottomToTopLeft** <br/> |19  <br/> |
|**visLOPlaceHierarchyBottomToTopRight** <br/> | 21  <br/> |
|**visLOPlaceHierarchyLeftToRightBottom** <br/> |24  <br/> |
|**visLOPlaceHierarchyLeftToRightMiddle** <br/> |23  <br/> |
|**visLOPlaceHierarchyLeftToRightTop** <br/> |22  <br/> |
|**visLOPlaceHierarchyRightToLeftBottom** <br/> |27  <br/> |
|**visLOPlaceHierarchyRightToLeftMiddle** <br/> |26  <br/> |
|**visLOPlaceHierarchyRightToLeftTop** <br/> |25  <br/> |
|**visLOPlaceHierarchyTopToBottomCenter** <br/> |17   <br/> |
|**visLOPlaceHierarchyTopToBottomLeft** <br/> |16   <br/> |
|**visLOPlaceHierarchyTopToBottomRight** <br/> |18   <br/> |
|**visLOPlaceLeftToRight** <br/> |2  <br/> |
|**visLOPlaceParentDefault** <br/> |15   <br/> |
|**visLOPlaceRadial** <br/> |3  <br/> |
|**visLOPlaceRightToLeft** <br/> |5  <br/> |
|**visLOPlaceTopToBottom** <br/> |1  <br/> |
   
To refer to the ShapePlaceStyle cell by name from another formula, or from a program using the **CellsU** property, use: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapePlaceStyle  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um anhand eines Indexes aus einem Programm auf die Zelle ShapePlaceStyle zu verweisen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOPlaceStyle** <br/> |
   

