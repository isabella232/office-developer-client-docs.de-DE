---
title: Zelle "Y" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026934
ms.localizationpriority: medium
ms.assetid: b213fc46-7f80-99fd-60ba-8ddf3d0f6ee3
description: Die Position der y-Koordinate in den lokalen Koordinaten des Shapes, um die sich die Schaltfläche des Aktionstags befindet.
ms.openlocfilehash: e6171370600beedc931d31b87b3a1dfd96d51a3e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582540"
---
# <a name="y-cell-action-tags-section"></a>Zelle "Y" (Abschnitt "Action Tags")

Die Position der y-Koordinate in den lokalen Koordinaten des Shapes, um die sich die Schaltfläche des Aktionstags befindet.  
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Zellen X und Y definieren einen Punkt in den lokalen Koordinaten des Shapes, und die Zellen X Justify und Y Justify definieren, wo die Schaltfläche Aktionstag in Bezug auf diesen Punkt platziert werden soll. 
  
Um einen Verweis auf die Zelle Y anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SmartTags.  *Name*  . Y, wobei SmartTags. *Name*  ist der Name der Aktionstagzeile  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Y anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**visRowSmartTag**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagY** <br/> |
   

