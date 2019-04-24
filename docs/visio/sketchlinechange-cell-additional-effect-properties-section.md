---
title: SketchLineChange Cell (Additional Effect Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Bestimmt den Grad der Zufallsgenerierung der Linie der Form aus der Geometrie der Form bei Verwendung eines Skizzen Effekts als Prozentsatz der Länge eines Abschnitts. Wenn der Wert der Zelle SketchLineChange auf 0% festgelegt ist, stimmt die Geometrie der Formlinie mit der Geometrie der Form überein. Wenn der Wert 100% ist, folgt die Geometrie der Formlinie nicht der Geometrie der Form.
ms.openlocfilehash: ba57a4d2e43a91475f4c3ab4862f723eb2653a89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315127"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a>SketchLineChange Cell (Additional Effect Properties section)

Bestimmt den Grad der Zufallsgenerierung der Linie der Form aus der Geometrie der Form bei Verwendung eines Skizzen Effekts als Prozentsatz der Länge eines Abschnitts. Wenn der Wert der Zelle **SketchLineChange** auf 0% festgelegt ist, stimmt die Geometrie der Formlinie mit der Geometrie der Form überein. Wenn der Wert 100% ist, folgt die Geometrie der Formlinie nicht der Geometrie der Form. 
  
## <a name="remarks"></a>Bemerkungen

Optimale Ergebnisse erzielen Sie, wenn der optimale Wert für die **SketchLineChange** -Zelle zwischen 15% und 50% liegt. Ein Wert unter 15% ist kaum spürbar; ein Wert, der größer als 50% ist, kann die Leitung zu stark randomizen. 
  
Wenn Sie einen Verweis auf die Zelle **SketchLineChange** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchLineChange  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **SketchLineChange** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchLineChange** <br/> |
   

