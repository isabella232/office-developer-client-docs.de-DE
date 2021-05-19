---
title: Zelle "EventXFMod" (Abschnitt "Events")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251313
localization_priority: Normal
ms.assetid: b88588a2-c651-7eab-9c7a-ed78f20d1ba3
description: Eine Ereigniszelle, die ausgewertet wird, wenn die Position oder Ausrichtung eines Shapes auf der Seite transformiert wird (XF).
ms.openlocfilehash: c4ed4ddd9b255a9a52fc81349b514dbd25772c98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418533"
---
# <a name="eventxfmod-cell-events-section"></a>Zelle "EventXFMod" (Abschnitt "Events")

Eine Ereigniszelle, die ausgewertet wird, wenn die Position oder Ausrichtung eines Shapes auf dem Blatt transformiert wird ("XF").
  
## <a name="remarks"></a>Hinweise

Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.
  
Um einen Verweis auf die EventXFMod-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | EventXFMod  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die EventXFMod-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowEvent** <br/> |
| Zeilenindex:  <br/> |**visEvtCellXFMod** <br/> |
   

