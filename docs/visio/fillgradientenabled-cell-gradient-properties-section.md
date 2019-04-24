---
title: Zelle "FillGradientEnabled" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: Bestimmt, ob ein Füll Verlauf für dieses Shape aktiviert ist.
ms.openlocfilehash: 17f617c13b632318be22b86a3354a194f0f835f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322491"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a>Zelle "FillGradientEnabled" (Abschnitt "Gradient Properties")

Bestimmt, ob ein Füll Verlauf für dieses Shape aktiviert ist. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die Farbverlaufsfüllung wird auf dem Shape angezeigt.  <br/> |
|FALSE  <br/> |Farbverlaufsfüllungen werden nicht auf dem Shape angezeigt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **FillGradientEnabled** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | FillGradientEnabled  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **FillGradientEnabled** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGradientProperties** <br/> |
| Zellenindex:  <br/> |* * visFillGradientEnabled * * <br/> |
   

