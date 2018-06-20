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
ms.openlocfilehash: 623d1d095d3269cd9c82fa8d0d6601933a163f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796946"
---
# <a name="eventdblclick-cell-events-section"></a>Zelle "EventDblClick" (Abschnitt "Events")

Eine Ereigniszelle, die ausgewertet wird, wenn Sie auf ein Shape doppelklicken.
  
## <a name="remarks"></a>Hinweise

Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.
  
Wenn Sie einen Verweis auf die Zelle EventDblClick nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | EventDblClick  <br/> |
   
Wenn Sie einen Verweis auf die Zelle EventDblClick aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowEvent** <br/> |
| Zellenindex:  <br/> |**visEvtCellDblClick** <br/> |
   

