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
ms.openlocfilehash: 858d98c8ee55eb49f58bbe98491ddc8752e75504
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796921"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a>DynFeedback Cell (Miscellaneous Section)

Ändert die Art des visuellen Feedbacks, das Benutzern angezeigt wird, wenn sie einen Verbinder mit der Maus verschieben. Wenn die Maustaste losgelassen wird, ist das daraus resultierende Verbinder-Shape von dieser Einstellung nicht betroffen. Diese Einstellung gilt nicht für umleitbare Verbinder.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Bleibt gerade (keine Abschnitte).  <br/> |**visDynFBDefault** <br/> |
| 1  <br/> | Zeigt beim Ziehen drei Abschnitte an.  <br/> |**visDynFBUCon3Leg** <br/> |
| 2  <br/> | Zeigt beim Ziehen fünf Abschnitte an.  <br/> |**visDynFBUCon5Leg** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle DynFeedback aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DynFeedback  <br/> |
   
Wenn Sie einen Verweis auf die Zelle DynFeedback aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visDynFeedback** <br/> |
   

