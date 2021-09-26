---
title: Zelle "DynFeedback" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251317
ms.localizationpriority: medium
ms.assetid: 44017319-7146-3431-e476-fbb1a40341ca
description: Ändert die Art des visuellen Feedbacks, das Benutzern angezeigt wird, wenn sie einen Verbinder mit der Maus verschieben. Wenn die Maustaste losgelassen wird, ist das daraus resultierende Verbinder-Shape von dieser Einstellung nicht betroffen. Diese Einstellung gilt nicht für umleitbare Verbinder.
ms.openlocfilehash: cc4f9d66cf06150f749cef28a83d212f232d866d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619120"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a>Zelle "DynFeedback" (Abschnitt "Miscellaneous")

Ändert die Art des visuellen Feedbacks, das Benutzern angezeigt wird, wenn sie einen Verbinder mit der Maus verschieben. Wenn die Maustaste losgelassen wird, ist das daraus resultierende Verbinder-Shape von dieser Einstellung nicht betroffen. Diese Einstellung gilt nicht für umleitbare Verbinder.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Bleibt gerade (keine Abschnitte).  <br/> |**visDynFBDefault** <br/> |
| 1  <br/> | Zeigt beim Ziehen drei Abschnitte an.  <br/> |**visDynFBUCon3Leg** <br/> |
| 2  <br/> | Zeigt beim Ziehen fünf Abschnitte an.  <br/> |**visDynFBUCon5Leg** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um einen Verweis auf die Zelle DynFeedback anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DynFeedback  <br/> |
   
Um einen Verweis auf die Zelle DynFeedback anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visDynFeedback** <br/> |
   

