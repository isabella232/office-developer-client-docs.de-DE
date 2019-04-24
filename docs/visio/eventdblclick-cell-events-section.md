---
title: Zelle "EventDblClick" (Abschnitt "Events")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251312
localization_priority: Normal
ms.assetid: ca949013-f998-1bce-39e5-ac6f68ab2392
description: Eine Ereigniszelle, die ausgewertet wird, wenn Sie auf ein Shape doppelklicken.
ms.openlocfilehash: a50e88ecd8e432629e246f7038dfcc9626725cc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337170"
---
# <a name="eventdblclick-cell-events-section"></a>Zelle "EventDblClick" (Abschnitt "Events")

Eine Ereigniszelle, die ausgewertet wird, wenn Sie auf ein Shape doppelklicken.
  
## <a name="remarks"></a>Bemerkungen

Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.
  
Wenn Sie einen Verweis auf die Zelle EreignisDpplKlck aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | EreignisDpplKlck  <br/> |
   
Wenn Sie einen Verweis auf die Zelle EreignisDpplKlck aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowEvent** <br/> |
| Zeilenindex:  <br/> |**visEvtCellDblClick** <br/> |
   

