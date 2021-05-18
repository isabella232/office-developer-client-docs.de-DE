---
title: Zelle "ShapeShdwObliqueAngle" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033174
localization_priority: Normal
ms.assetid: bad4c512-e91f-d459-d65c-a4ab725c3c14
description: Gibt den Winkel der Schrägrichtung des Shape-Schattens an.
ms.openlocfilehash: 005415e497a4d985d3fb8ec70d62ba40d9e80c91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414032"
---
# <a name="shapeshdwobliqueangle-cell-fill-format-section"></a>Zelle "ShapeShdwObliqueAngle" (Abschnitt "Fill Format")

Gibt den Winkel der Schrägrichtung des Shape-Schattens an.
  
## <a name="remarks"></a>Hinweise

Der Wert Null (0) in dieser Zelle zeigt an, dass die Winkelrichtung genau nach oben verläuft, sie wird im Uhrzeigersinn gemessen.
  
Dieser Wert entspricht dem Wert der Einstellung **Richtung** im Dialogfeld **Schatten** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**).
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle ShapeShdwObliqueAngle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShapeShdwObliqueAngle  <br/> |
   
Um einen Verweis auf die Zelle ShapeShdwObliqueAngle nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowFill** <br/> |
| Zellenindex:  <br/> |**visFillShdwObliqueAngle** <br/> |
   

