---
title: Zelle "ShdwScaleFactor" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60083
localization_priority: Normal
ms.assetid: 10979706-6dfe-5241-e862-3f94716d14fa
description: Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert wird.
ms.openlocfilehash: 9175e9a1148779524fdce96ff18eac22fe8dd421
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342882"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a>Zelle "ShdwScaleFactor" (Abschnitt "Page Properties")

Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert wird. 
  
## <a name="remarks"></a>Bemerkungen

Jeder Schatten hat eine schattierte Pin-Position, die ein Punkt auf dem Schatten ist, der der PIN des Shapes entspricht. Wenn sich beispielsweise die PIN eines Shapes in der Mitte des Shapes befindet, ist die schattierte Position des Pins der Punkt in der Mitte des Schattens. Wenn Sie die Skalierung auf einfache Schatten anwenden, wird die Vergrößerung an der schattierten Pin-Position zentriert. Wenn Sie die Skalierung auf schräge Schatten anwenden, wird die Vergrößerung in schräger Richtung angewendet. 
  
 Dieser Prozentsatz wird verwendet, wenn der Schattentyp für ein Shape auf Seiten Standard festgelegt ist (Zelle Cell Equals * * visFSTPageDefault * *). 
  
Wenn Sie dieses Verhalten für einen einzelnen Schatten festlegen möchten, verwenden Sie im Abschnitt Fill Format die Zelle ShapeShdwScaleFactor.
  
Dieser Wert entspricht dem Wert, den Sie im Dialogfeld **Seite einrichten** auf der Registerkarte **Schatten** im Feld **Vergrößerung** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). 
  
Wenn Sie einen Verweis auf die Zelle "ShdwScaleFactor aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | "ShdwScaleFactor  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "ShdwScaleFactor aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageShdwScaleFactor** <br/> |
   

