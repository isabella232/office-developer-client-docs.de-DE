---
title: Zelle "X" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60093
localization_priority: Normal
ms.assetid: d13e362b-9b69-30c5-003a-9c5df2aa29f6
description: Die x-Koordinate in den lokalen Koordinaten des Shapes, um die sich die Schaltfläche Aktionstag befindet.
ms.openlocfilehash: 9f26bec81563c9813a88ed5c69730266834ee101
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431113"
---
# <a name="x-cell-action-tags-section"></a>Zelle "X" (Abschnitt "Action Tags")

Die *x* -Koordinate in den lokalen Koordinaten des Shapes, um die sich die Schaltfläche Aktionstag befindet. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>Bemerkungen

Die Zellen X und Y definieren einen Punkt in den lokalen Koordinaten des Shapes, und die Zellen X Justify und Y Justify definieren, wo die Schaltfläche Aktionstag in Bezug auf diesen Punkt platziert werden soll. 
  
Wenn Sie einen Verweis auf die Zelle X aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> |Smarttags. *Name* . X, wobei SmartTags. *Name* ist der Name der Zeile mit dem Aktionstag.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle X aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**visRowSmartTag** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagX** <br/> |
   

