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
ms.openlocfilehash: 11f172de33dfbb65d0176733f5c0bf8b33db483d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798037"
---
# <a name="shapeshdwobliqueangle-cell-fill-format-section"></a>ShapeShdwObliqueAngle Cell (Fill Format Section)

Gibt den Winkel der Schrägrichtung des Shape-Schattens an.
  
## <a name="remarks"></a>Bemerkungen

Der Wert Null (0) in dieser Zelle zeigt an, dass die Winkelrichtung genau nach oben verläuft, sie wird im Uhrzeigersinn gemessen.
  
Dieser Wert entspricht dem Wert der Einstellung **Richtung** im Dialogfeld **Schatten** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**).
  
Wenn Sie einen Verweis auf die Zelle ShapeShdwObliqueAngle aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShapeShdwObliqueAngle  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ShapeShdwObliqueAngle aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowFill** <br/> |
| Zellenindex:  <br/> |**visFillShdwObliqueAngle** <br/> |
   

