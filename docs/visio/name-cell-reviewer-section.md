---
title: Zelle "Name" (Abschnitt "Reviewer")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030992
localization_priority: Normal
ms.assetid: be39cd0b-56bf-a070-f5d8-c9a440d81ee2
description: Enthält den Namen des Bearbeiters eines Dokuments.
ms.openlocfilehash: 02f353ab8f2d39cc075211bb13157b93081e9d8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417686"
---
# <a name="name-cell-reviewer-section"></a>Zelle "Name" (Abschnitt "Reviewer")

Enthält den Namen des Bearbeiters eines Dokuments.
  
## <a name="remarks"></a>Hinweise

 Dieser Wert wird standardmäßig auf  den Namen im Feld Benutzername auf der Registerkarte  **Allgemein** des Dialogfelds **Visio-Optionen** festgelegt (klicken Sie auf die Registerkarte Datei, klicken Sie auf **Optionen** und dann auf **Allgemein**). 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle Name anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Reviewer.Name [  *i*  ] wobei  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Name nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionReviewer** <br/> |
| Zeilenindex:  <br/> |**visRowReviewer**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visReviewerName** <br/> |
   

