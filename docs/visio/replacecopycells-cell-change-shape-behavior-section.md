---
title: Zelle "ReplaceCopyCells" (Abschnitt "Change Shape Behavior")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Gibt eine Liste der Zellen im ShapeSheet an, die während eines Shape-Ersetzungsvorgangs von einem alten Shape in das Ersetzungs-Shape kopiert werden.
ms.openlocfilehash: 498bf18e2e0beaf31d2673687dd5d2abe0ced2c1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607815"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a>Zelle "ReplaceCopyCells" (Abschnitt "Change Shape Behavior")

Gibt eine Liste der Zellen im ShapeSheet an, die während eines Shape-Ersetzungsvorgangs von einem alten Shape in das Ersetzungs-Shape kopiert werden. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Masterform der Ersetzung muss einen **DEPENDSON-Funktionsaufruf** in der Zelle **ReplaceCopyCells** enthalten, wobei jedes Argument in der Funktion ein Bezug auf eine Zelle ist. Diese Zellen werden vom alten Shape in das Shape kopiert, das sich aus einem Shape-Ersetzungsvorgang ergibt, unabhängig davon, wo sie sich im ShapeSheet befinden. 
  
Werte und/oder Formeln, die auf andere Zellen verweisen, werden in das resultierende Shape kopiert. Wenn die resultierende Form nicht über die Zelle verfügt, auf die verwiesen wird, enthält die kopierte Zelle nur den Wert. 
  
Verweise in der **Zelle "ReplaceCopyCells"** setzen den Schutz für Zellen außer Kraft, wie im Abschnitt **"Protection"** und in den Zellen **"ReplaceLockFormat",** **"ReplaceLockShapeData"** und **"ReplaceLockText"** definiert. 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle **"ReplaceCopyCells"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ReplaceCopyCells  <br/> |
   
Um einen Verweis auf die Zelle **"ReplaceCopyCells"** anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowReplaceBehaviors** <br/> |
| Zellenindex:  <br/> |**visReplaceCopyCells** <br/> |
   

