---
title: Zelle "ShapeShdwScaleFactor" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033175
localization_priority: Normal
ms.assetid: 94ec06c5-8d2f-dd27-1eed-1abaf93daba8
description: Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert werden kann.
ms.openlocfilehash: 0b6392030e7efc8ea36c8d728b99c9b82482840b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798061"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a>ShapeShdwScaleFactor Cell (Fill Format Section)

Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert werden kann.
  
## <a name="remarks"></a>Bemerkungen

Jeder Schatten weist eine schattierte Speicherorts eines Punkts auf der Schatten, die die Shape-PIN bis entspricht. Wenn ein Shape-Pin in der Mitte des Shapes befindet, würde der schattierte Speicherort beispielsweise den Punkt in der Mitte des Schattens sein. Skalierung auf einfache Schatten angewendet wird, wird an der Position schattierte Vergrößerung zentriert; Beim Skalieren einfache Schatten anwenden, wird die Vergrößerung in der Schräge angibt angewendet. 
  
Wenn Sie diesen Wert für alle Shapes auf einem Zeichenblatt festlegen möchten, verwenden Sie die Zelle ShapeShdwScaleFactor im Abschnitt Page Properties.
  
Dieser Wert entspricht dem Wert der Einstellung **Vergrößerung** im Dialogfeld **Schatten** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**).
  
Wenn Sie einen Verweis auf die Zelle ShapeShdwScaleFactor aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapeShdwScaleFactor  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ShapeShdwScaleFactor aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowFill** <br/> |
|Zellenindex:  <br/> |**visFillShdwScaleFactor** <br/> |
   

