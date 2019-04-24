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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326677"
---
# <a name="thetext-cell-events-section"></a>Zelle "TheText" (Abschnitt "Events")

Eine Ereigniszelle, die berechnet wird, wenn der Text oder die Textgestaltung eines Shapes geändert wird.
  
## <a name="remarks"></a>Bemerkungen

Ereigniszellen werden nur beim Eintreffen des Ereignisses, nicht bei der Formeleingabe ausgewertet. Sie können die Zelle TheText verwenden, um Neuberechnungen zu starten, beispielsweise um die Textbreite und -höhe mithilfe der Funktionen TEXTWIDTH( ) und TEXTHÖHE( ) neu zu berechnen.
  
Wenn Sie einen Verweis auf die Zelle DerText aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DerText  <br/> |
   
Wenn Sie einen Verweis auf die Zelle DerText aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowEvent** <br/> |
| Zellenindex:  <br/> |**visEvtCellTheText** <br/> |
   

