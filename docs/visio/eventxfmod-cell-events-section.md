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
description: Eine Ereignis Zelle, die ausgewertet wird, wenn sich die Position oder Ausrichtung der Form auf der Seite wandelt (XF).
ms.openlocfilehash: c4ed4ddd9b255a9a52fc81349b514dbd25772c98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350974"
---
# <a name="eventxfmod-cell-events-section"></a>Zelle "EventXFMod" (Abschnitt "Events")

Eine Ereigniszelle, die ausgewertet wird, wenn die Position oder Ausrichtung eines Shapes auf dem Blatt transformiert wird ("XF").
  
## <a name="remarks"></a>Bemerkungen

Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.
  
Wenn Sie einen Verweis auf die Zelle "EventXFMod aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | "EventXFMod  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "EventXFMod aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowEvent** <br/> |
| Zeilenindex:  <br/> |**visEvtCellXFMod** <br/> |
   

