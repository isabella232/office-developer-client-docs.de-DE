---
title: Zelle "EventDrop" (Abschnitt "Events")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm350
localization_priority: Normal
ms.assetid: f84afe83-8391-0c13-f442-ea8794b38642
description: Eine Ereigniszelle, die ausgewertet wird, wenn ein Shape als Instanz auf dem Zeichenblatt abgelegt oder dupliziert oder eingefügt wird.
ms.openlocfilehash: e2624c50896de061727003a48f7dc1559c6a72c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796944"
---
# <a name="eventdrop-cell-events-section"></a>Zelle "EventDrop" (Abschnitt "Events")

Eine Ereigniszelle, die ausgewertet wird, wenn ein Shape als Instanz auf dem Zeichenblatt abgelegt oder dupliziert oder eingefügt wird.
  
## <a name="remarks"></a>Hinweise

Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.
  
Wenn Sie einen Verweis auf die Zelle EventDrop nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | EventDrop  <br/> |
   
Wenn Sie einen Verweis auf die Zelle EventDrop aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowEvent** <br/> |
| Zellenindex:  <br/> |**visEvtCellDrop** <br/> |
   

