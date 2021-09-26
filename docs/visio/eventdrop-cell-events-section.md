---
title: Zelle "EventDrop" (Abschnitt "Events")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm350
ms.localizationpriority: medium
ms.assetid: f84afe83-8391-0c13-f442-ea8794b38642
description: Eine Ereigniszelle, die ausgewertet wird, wenn ein Shape als Instanz auf dem Zeichenblatt abgelegt oder dupliziert oder eingefügt wird.
ms.openlocfilehash: a2e65d4a62f9323580913c0d23eb4b15aa0835e9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619085"
---
# <a name="eventdrop-cell-events-section"></a>Zelle "EventDrop" (Abschnitt "Events")

Eine Ereigniszelle, die ausgewertet wird, wenn ein Shape als Instanz auf dem Zeichenblatt abgelegt oder dupliziert oder eingefügt wird.
  
## <a name="remarks"></a>Bemerkungen

Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.
  
Um einen Verweis auf die Zelle EventDrop anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | EventDrop  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle EventDrop anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowEvent** <br/> |
| Zeilenindex:  <br/> |**visEvtCellDrop** <br/> |
   

