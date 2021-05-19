---
title: Zelle "EventMultiDrop" (Abschnitt "Events")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: caa86e33d0d7aa9ca31cbbf8939e17b581877669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416720"
---
# <a name="eventmultidrop-cell-events-section"></a>Zelle "EventMultiDrop" (Abschnitt "Events")

Eine Ereigniszelle, die ausgewertet wird, wenn mehrere Shapes auf dem Zeichenblatt abgelegt werden, entweder als Instanzen oder wenn Shapes dupliziert oder eingelassen werden.
  
Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.
  
Verwenden Sie zum Verweisen auf die EventMultiDrop-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |EventMultiDrop  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um auf die EventMultiDrop-Zelle nach Index aus einem Programm zu verweisen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowEvent** <br/> |
|Zellenindex:  <br/> |**visEvtCellMultiDrop** <br/> |
   

