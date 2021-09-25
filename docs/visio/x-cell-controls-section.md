---
title: Zelle "X" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251281
ms.localizationpriority: medium
ms.assetid: b7aea554-f491-6a9a-4d07-feeab739a9df
description: Stellt die x-Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten angibt.
ms.openlocfilehash: 948b27415d22f4beb2d4c6d0c3a14e53252920f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582521"
---
# <a name="x-cell-controls-section"></a>Zelle "X" (Abschnitt "Controls")

Stellt  die x-Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten angibt. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle X anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name*  . X where Controls.  *Name*  ist der Name der Steuerelementzeile.  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle X anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionControls** <br/> |
| Zeilenindex:  <br/> |**visRowControl**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCtlX** <br/> |
   

