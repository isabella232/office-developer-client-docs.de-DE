---
title: Zelle "TheText" (Abschnitt "Events")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1005
localization_priority: Normal
ms.assetid: 2d63768e-afdb-4b3f-de49-f9ba69ae5391
description: Eine Ereigniszelle, die berechnet wird, wenn der Text oder die Textgestaltung eines Shapes geändert wird.
ms.openlocfilehash: 942ccee4478c87243207d8d65785857758d2a068
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798271"
---
# <a name="thetext-cell-events-section"></a>TheText Cell (Events Section)

Eine Ereigniszelle, die berechnet wird, wenn der Text oder die Textgestaltung eines Shapes geändert wird.
  
## <a name="remarks"></a>Hinweise

Ereigniszellen werden nur beim Eintreffen des Ereignisses, nicht bei der Formeleingabe ausgewertet. Sie können die Zelle TheText verwenden, um Neuberechnungen zu starten, beispielsweise um die Textbreite und -höhe mithilfe der Funktionen TEXTWIDTH( ) und TEXTHÖHE( ) neu zu berechnen.
  
Wenn Sie einen Verweis auf die Zelle TheText aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TheText  <br/> |
   
Wenn Sie einen Verweis auf die Zelle TheText aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowEvent** <br/> |
| Zellenindex:  <br/> |**visEvtCellTheText** <br/> |
   

