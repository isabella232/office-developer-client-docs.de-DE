---
title: SoftEdgesSize Cell (Additional Effect Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a5cde2ca-f343-4a6e-b5d9-a1b78b3cd240
description: Bestimmt die Größe eines weichen Kanten Effekts in Punkt von 0,00 bis 100,00. Wenn die Zelle SoftEdgesSize den Wert 0 hat, weist die Form keine weichen Ränder auf.
ms.openlocfilehash: e749fefde8e0358cbf4ab8388a61ad703c7d52ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334538"
---
# <a name="softedgessize-cell-additional-effect-properties-section"></a>SoftEdgesSize Cell (Additional Effect Properties section)

Bestimmt die Größe eines weichen Kanten Effekts in Punkt von 0,00 bis 100,00. Wenn die Zelle **SoftEdgesSize** den Wert 0 hat, weist die Form keine weichen Ränder auf. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **SoftEdgesSize** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SoftEdgesSize  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **SoftEdgesSize** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSoftEdgesSize** <br/> |
   

