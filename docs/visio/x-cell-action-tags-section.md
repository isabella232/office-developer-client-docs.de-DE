---
title: Zelle "X" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60093
ms.localizationpriority: medium
ms.assetid: d13e362b-9b69-30c5-003a-9c5df2aa29f6
description: Die X-Koordinatenposition in den lokalen Koordinaten des Shapes, um die die Aktionstagschaltfläche platziert wird.
ms.openlocfilehash: 76b334daf087fd2fcacf1fd706cfb3186e87110c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603193"
---
# <a name="x-cell-action-tags-section"></a>Zelle "X" (Abschnitt "Action Tags")

Die  X-Koordinatenposition in den lokalen Koordinaten des Shapes, um die die Aktionstagschaltfläche platziert wird. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Zellen X und Y definieren einen Punkt in den lokalen Koordinaten des Shapes, und die Zellen X Justify und Y Justify definieren, wo die Schaltfläche Aktionstag in Bezug auf diesen Punkt platziert werden soll. 
  
Um einen Verweis auf die Zelle X anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> |SmartTags. *Name*  . X, wobei SmartTags. *Name*  ist der Name der Aktionstagzeile  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle X anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**visRowSmartTag**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagX** <br/> |
   

