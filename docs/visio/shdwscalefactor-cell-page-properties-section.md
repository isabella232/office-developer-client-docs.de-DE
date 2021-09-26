---
title: Zelle "ShdwScaleFactor" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60083
ms.localizationpriority: medium
ms.assetid: 10979706-6dfe-5241-e862-3f94716d14fa
description: Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert wird.
ms.openlocfilehash: bc5f5fb3fa4fc3d922c0ac8e629f784212a5e3c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603522"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a>Zelle "ShdwScaleFactor" (Abschnitt "Page Properties")

Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert wird. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Jeder Schatten hat eine schattierte Pin-Position, die ein Punkt auf dem Schatten ist, der dem Pin des Shapes entspricht. Wenn sich beispielsweise der Drehpunkt eines Shapes in der Mitte der Form befindet, ist die Position des schattierten Pins der Punkt in der Mitte des Schattens. Beim Anwenden von Skalierung auf einfache Schatten wird die Vergrößerung an der Position des schattierten Pins zentriert. Beim Anwenden von Skalierung auf schräge Schatten wird die Vergrößerung in schräger Richtung angewendet. 
  
 Dieser Prozentsatz wird verwendet, wenn der Schattentyp für ein Shape auf Page Default festgelegt ist (ShapeShdwType cell equals ** visFSTPageDefault ** ). 
  
Wenn Sie dieses Verhalten für einen einzelnen Schatten festlegen möchten, verwenden Sie im Abschnitt Fill Format die Zelle ShapeShdwScaleFactor.
  
Dieser Wert entspricht dem Wert, den Sie im Dialogfeld **Seite einrichten** auf der Registerkarte **Schatten** im Feld **Vergrößerung** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). 
  
Um einen Verweis auf die Zelle "ShdwScaleFactor" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShdwScaleFactor  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShdwScaleFactor anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageShdwScaleFactor** <br/> |
   

