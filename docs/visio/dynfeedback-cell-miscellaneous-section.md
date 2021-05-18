---
title: Zelle "DynFeedback" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251317
localization_priority: Normal
ms.assetid: 44017319-7146-3431-e476-fbb1a40341ca
description: Ändert die Art des visuellen Feedbacks, das Benutzern angezeigt wird, wenn sie einen Verbinder mit der Maus verschieben. Wenn die Maustaste losgelassen wird, ist das daraus resultierende Verbinder-Shape von dieser Einstellung nicht betroffen. Diese Einstellung gilt nicht für umleitbare Verbinder.
ms.openlocfilehash: 823b8db4dc6afe94a5fdac1f62aaa48d7e1b0d80
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404799"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a>Zelle "DynFeedback" (Abschnitt "Miscellaneous")

Ändert die Art des visuellen Feedbacks, das Benutzern angezeigt wird, wenn sie einen Verbinder mit der Maus verschieben. Wenn die Maustaste losgelassen wird, ist das daraus resultierende Verbinder-Shape von dieser Einstellung nicht betroffen. Diese Einstellung gilt nicht für umleitbare Verbinder.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Bleibt gerade (keine Abschnitte).  <br/> |**visDynFBDefault** <br/> |
| 1  <br/> | Zeigt beim Ziehen drei Abschnitte an.  <br/> |**visDynFBUCon3Leg** <br/> |
| 2  <br/> | Zeigt beim Ziehen fünf Abschnitte an.  <br/> |**visDynFBUCon5Leg** <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die DynFeedback-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DynFeedback  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die DynFeedback-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visDynFeedback** <br/> |
   

