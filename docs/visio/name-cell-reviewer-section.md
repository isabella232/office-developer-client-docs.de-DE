---
title: Zelle "Name" (Abschnitt "Reviewer")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030992
ms.localizationpriority: medium
ms.assetid: be39cd0b-56bf-a070-f5d8-c9a440d81ee2
description: Enthält den Namen des Bearbeiters eines Dokuments.
ms.openlocfilehash: 7f04882b5b5ba8bfed3a275b3700164c52d23cf4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563021"
---
# <a name="name-cell-reviewer-section"></a>Zelle "Name" (Abschnitt "Reviewer")

Enthält den Namen des Bearbeiters eines Dokuments.
  
## <a name="remarks"></a>HinwBemerkungeneise

 Dieser Wert ist standardmäßig auf den Namen im **Feld "Benutzername"** auf der Registerkarte **"Allgemein"** des Dialogfelds **Visio Optionen** festgelegt (klicken Sie auf die Registerkarte **"Datei",** auf **"Optionen"** und dann auf **"Allgemein").** 
  
Um einen Verweis auf die Zelle "Name" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Reviewer.Name [  *i*  ] wobei  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Name anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionReviewer** <br/> |
| Zeilenindex:  <br/> |**visRowReviewer**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visReviewerName** <br/> |
   

