---
title: SoftEdgesSize Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a5cde2ca-f343-4a6e-b5d9-a1b78b3cd240
description: Bestimmt die Größe des ein weichen Kanteneffekt in Punkt von 0,00 zu 100.00. Wenn die Zelle SoftEdgesSize den Wert 0 hat, verfügt die Form nicht weiche Kanten.
ms.openlocfilehash: 3b301ae2e8c82867be2a486f2e93c2275fbf3914
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798161"
---
# <a name="softedgessize-cell-additional-effect-properties-section"></a>SoftEdgesSize Cell (Additional Effect Properties Section)

Bestimmt die Größe des ein weichen Kanteneffekt in Punkt von 0,00 zu 100.00. Wenn die Zelle **SoftEdgesSize** den Wert 0 hat, verfügt die Form nicht weiche Kanten. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **SoftEdgesSize** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SoftEdgesSize  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **SoftEdgesSize** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSoftEdgesSize** <br/> |
   

