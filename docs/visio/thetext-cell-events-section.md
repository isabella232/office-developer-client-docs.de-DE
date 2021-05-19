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
ms.openlocfilehash: 6aa5e14f339d0030d8421eaae62b0e481be91fc7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435166"
---
# <a name="thetext-cell-events-section"></a>Zelle "TheText" (Abschnitt "Events")

Eine Ereigniszelle, die berechnet wird, wenn der Text oder die Textgestaltung eines Shapes geändert wird.
  
## <a name="remarks"></a>Hinweise

Ereigniszellen werden nur beim Eintreffen des Ereignisses, nicht bei der Formeleingabe ausgewertet. Sie können die Zelle TheText verwenden, um Neuberechnungen zu starten, beispielsweise um die Textbreite und -höhe mithilfe der Funktionen TEXTWIDTH( ) und TEXTHÖHE( ) neu zu berechnen.
  
Um einen Verweis auf die Zelle TheText anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TheText  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle TheText nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowEvent** <br/> |
| Zellenindex:  <br/> |**visEvtCellTheText** <br/> |
   

