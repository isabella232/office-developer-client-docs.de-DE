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
ms.openlocfilehash: 5862b61ca1f5df25ca97bf8742b9e20bf45091a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436265"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a>Zelle "ShapeShdwScaleFactor" (Abschnitt "Fill Format")

Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert werden kann.
  
## <a name="remarks"></a>Hinweise

Jeder Schatten hat eine verschattene Pinposition, bei der es sich um einen Punkt auf dem Schatten handelt, der dem Pin des Shapes entspricht. Wenn sich z. B. der Pin eines Shapes in der Mitte der Form befindet, wäre die position des schattierten Stifts der Punkt in der Mitte des Schattens. Beim Anwenden der Skalierung auf einfache Schatten wird die Vergrößerung an der position des schattierten Stifts zentriert. Beim Anwenden der Skalierung auf schräge Schatten wird die Vergrößerung in schräger Richtung angewendet. 
  
Wenn Sie diesen Wert für alle Shapes auf einem Zeichenblatt festlegen möchten, verwenden Sie die Zelle ShapeShdwScaleFactor im Abschnitt Page Properties.
  
Dieser Wert entspricht dem Wert der Einstellung **Vergrößerung** im Dialogfeld **Schatten** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**).
  
Um einen Verweis auf die Zelle ShapeShdwScaleFactor anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapeShdwScaleFactor  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapeShdwScaleFactor nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowFill** <br/> |
|Zellenindex:  <br/> |**visFillShdwScaleFactor** <br/> |
   

