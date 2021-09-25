---
title: Zelle "ReplaceLockFormat" (Abschnitt "Change Shape Behavior")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shape-Ersetzungsvorgangs ersetzt wird. Wenn die Zelle ReplaceLockFormat eines Master-Shapes auf TRUE (1) festgelegt ist, überschreiben die Formatierungswerte des Master-Shapes alle entsprechenden Werte eines Shapes, das durch das Master-Shape ersetzt wird.
ms.openlocfilehash: 2e5f7bb373416ed99f7d4f14cba3aba015243940
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559682"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a>Zelle "ReplaceLockFormat" (Abschnitt "Change Shape Behavior")

Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shape-Ersetzungsvorgangs ersetzt wird. Wenn die Zelle **ReplaceLockFormat** eines Master-Shapes auf TRUE (1) festgelegt ist, überschreiben die Formatierungswerte des Master-Shapes alle entsprechenden Werte eines Shapes, das durch das Master-Shape ersetzt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Wenn die Zelle **"ReplaceLockFormat"** eines Master-Shapes auf TRUE festgelegt ist, überschreiben die Formatierungswerte des Master-Shapes alle entsprechenden Werte eines Shapes, das durch das Master-Shape ersetzt wird.  <br/> |
|FALSE  <br/> |Wenn die Zelle **ReplaceLockFormat** eines Master-Shapes auf FALSE festgelegt ist, enthält das Ersetzungs-Shape die lokalen Formatierungswerte der alten Form nach dem Ersetzungsvorgang.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Zelle **"ReplaceLockFormat"** bestimmt, ob das Master-Shape während eines Shape-Ersetzungsvorgangs die lokalen Formatierungswerte der Zellen in den folgenden Abschnitten überschreibt: 
  
- Abschnitt **"Fill Format"** 
    
- **Abschnitt "Line Format"** 
    
- **Abschnitt "Schnellformatvorlage"** 
    
- Abschnitt **"Theme Properties"** 
    
- **Abschnitt "Gradient Properties"** 
    
- Abschnitt **"Bevel Properties"** 
    
- **Abschnitt "Zusätzliche Effekteigenschaften"** 
    
- **Abschnitt "Line Gradient Stops"** 
    
- Abschnitt **"Fill Gradient Stops"** 
    
Verwenden Sie Folgendes, um einen Verweis auf die **Zelle "ReplaceLockFormat"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ReplaceLockFormat  <br/> |
   
Um einen Verweis auf die Zelle **"ReplaceLockFormat"** anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowReplaceBehaviors** <br/> |
| Zellenindex:  <br/> |**visReplaceLockFormat** <br/> |
   

