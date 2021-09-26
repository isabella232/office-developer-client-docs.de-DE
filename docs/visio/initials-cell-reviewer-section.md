---
title: Zelle "Initials" (Abschnitt "Reviewer")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
ms.localizationpriority: medium
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: Enthält die Initialen eines Dokumentbearbeiters.
ms.openlocfilehash: e3f76685631ca6ddba1848d8ecd57533755ecf84
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618805"
---
# <a name="initials-cell-reviewer-section"></a>Zelle "Initials" (Abschnitt "Reviewer")

Enthält die Initialen eines Dokumentbearbeiters.
  
## <a name="remarks"></a>Bemerkungen

Dieser Wert ist standardmäßig auf die Initialen im **Feld "Initialen"** auf der Registerkarte **"Allgemein"** im Dialogfeld **Visio Optionen** festgelegt (klicken Sie auf die Registerkarte **"Datei",** klicken Sie auf **"Optionen"** und dann auf **"Allgemein").** 
  
Um einen Verweis auf die Zelle "Initials" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Reviewer.Initials [  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Initials anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionReviewer** <br/> |
| Zeilenindex:  <br/> |**visRowReviewer**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visReviewerInitials** <br/> |
   

