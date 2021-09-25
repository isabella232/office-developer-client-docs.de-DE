---
title: Zelle "ShapeShdwScaleFactor" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033175
ms.localizationpriority: medium
ms.assetid: 94ec06c5-8d2f-dd27-1eed-1abaf93daba8
description: Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert werden kann.
ms.openlocfilehash: 3c68cb9aa7328078ce8d6c56da5297f98afdc908
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573327"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a>Zelle "ShapeShdwScaleFactor" (Abschnitt "Fill Format")

Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert werden kann.
  
## <a name="remarks"></a>HinwBemerkungeneise

Jeder Schatten hat eine schattierte Pin-Position, die ein Punkt auf dem Schatten ist, der dem Pin des Shapes entspricht. Wenn sich beispielsweise der Drehpunkt eines Shapes in der Mitte der Form befindet, ist die Position des schattierten Pins der Punkt in der Mitte des Schattens. Beim Anwenden von Skalierung auf einfache Schatten wird die Vergrößerung an der Position des schattierten Pins zentriert. Beim Anwenden von Skalierung auf schräge Schatten wird die Vergrößerung in schräger Richtung angewendet. 
  
Wenn Sie diesen Wert für alle Shapes auf einem Zeichenblatt festlegen möchten, verwenden Sie die Zelle ShapeShdwScaleFactor im Abschnitt Page Properties.
  
Dieser Wert entspricht dem Wert der Einstellung **Vergrößerung** im Dialogfeld **Schatten** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**).
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle ShapeShdwScaleFactor anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapeShdwScaleFactor  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapeShdwScaleFactor anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowFill** <br/> |
|Zellenindex:  <br/> |**visFillShdwScaleFactor** <br/> |
   

