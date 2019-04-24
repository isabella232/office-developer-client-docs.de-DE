---
title: Zelle "ButtonFace" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60026
localization_priority: Normal
ms.assetid: 26f370e1-5193-f47d-7b60-3597975be650
description: Enthält die ID der Schaltflächenoberseite, die auf der Schaltfläche Aktionstag angezeigt wird.
ms.openlocfilehash: e74b3281d894cebd8491112181198d427f0d337f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337538"
---
# <a name="buttonface-cell-action-tags-section"></a>Zelle "ButtonFace" (Abschnitt "Action Tags")

Enthält die ID der Schaltflächenoberseite, die auf der Schaltfläche Aktionstag angezeigt wird. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>Bemerkungen

Die Zeichenfolge in einer ButtonFace-Zelle stellt die ID einer Microsoft Office-Schaltflächenoberseite dar. Der Wert 0 (null) oder leer ist standardmäßig auf die Schaltfläche "i" Info. ![Standard Aktionstag "i" Info-Schaltfläche](media/InfoPS_ZA10180114.gif).
  
Die IDs, die in der "ButtonFace-Zelle verwendet werden können, sind identisch mit den IDs, die mit der **Face** -ID-Eigenschaft eines **CommandBarButton** -Objekts verwendet werden. Weitere Informationen zu diesen IDs finden Sie unter "Working with Command Bar Button Images" auf MSDN. 
  
Wenn Sie einen Verweis auf die Zelle "ButtonFace aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Smarttags.  *Name* . "ButtonFace, wobei SmartTags. *Name* ist der Name der Zeile mit dem Aktionstag.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "ButtonFace aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**visRowSmartTag** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagButtonFace** <br/> |
   

