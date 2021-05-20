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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429005"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a>Zelle "ShdwScaleFactor" (Abschnitt "Page Properties")

Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert wird. 
  
## <a name="remarks"></a>Hinweise

Jeder Schatten hat eine verschattene Pinposition, bei der es sich um einen Punkt auf dem Schatten handelt, der dem Pin des Shapes entspricht. Wenn sich z. B. der Pin eines Shapes in der Mitte der Form befindet, wäre die position des schattierten Stifts der Punkt in der Mitte des Schattens. Beim Anwenden der Skalierung auf einfache Schatten wird die Vergrößerung an der position des schattierten Stifts zentriert. Beim Anwenden der Skalierung auf schräge Schatten wird die Vergrößerung in schräger Richtung angewendet. 
  
 Dieser Prozentsatz wird verwendet, wenn der Schattentyp für ein Shape auf Page Default (ShapeShdwType cell equals ** visFSTPageDefault ** ) festgelegt ist. 
  
Wenn Sie dieses Verhalten für einen einzelnen Schatten festlegen möchten, verwenden Sie im Abschnitt Fill Format die Zelle ShapeShdwScaleFactor.
  
Dieser Wert entspricht dem Wert, den Sie im Dialogfeld **Seite einrichten** auf der Registerkarte **Schatten** im Feld **Vergrößerung** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). 
  
Um einen Verweis auf die ShdwScaleFactor-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShdwScaleFactor  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ShdwScaleFactor-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageShdwScaleFactor** <br/> |
   

