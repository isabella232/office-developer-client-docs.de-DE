---
title: Zelle "Y Dynamics" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
ms.localizationpriority: medium
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: Stellt die y-Koordinate für den Ankerpunkt eines Steuerpunkts in lokalen Koordinaten dar. Der Verankerungspunkt wird zum Rubber-Banding bei aktivierter Dynamik verwendet.
ms.openlocfilehash: 0e60b9e2233068bc950d4649ff261dcc92e8e1a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581742"
---
# <a name="y-dynamics-cell-controls-section"></a>Zelle "Y Dynamics" (Abschnitt "Controls")

Stellt  die y-Koordinate für den Ankerpunkt eines Steuerpunkts in lokalen Koordinaten dar. Der Verankerungspunkt wird zum "Rubber-Banding" bei aktivierter Dynamik verwendet. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie Folgendes, um einen Verweis auf die Zelle "Y Dynamics" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name*  . JJJNWHERE-Steuerelemente.  *Name*  ist der Name der Steuerelementzeile.  <br/> |
   
Um einen Verweis auf die Zelle Y Dynamics anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionControls** <br/> |
| Zeilenindex:  <br/> |**visRowControl**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCtlYDyn** <br/> |
   

