---
title: Zelle "TagName" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
localization_priority: Normal
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: Der Name des Aktionstags, das als Schlüssel verwendet wird, um das Aktionstag seinen Aktionen zuzuordnen.
ms.openlocfilehash: dbac3d4dff9d2ffd18bba75db56cafc08f5e0ee8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798226"
---
# <a name="tagname-cell-action-tags-section"></a>TagName Cell (Action Tags Section)

Der Name des Aktionstags, das als Schlüssel verwendet wird, um das Aktionstag seinen Aktionen zuzuordnen.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>Hinweise

 Die Zelle TagName im Abschnitt Action Tags kann zusammen mit der Zelle TagName im Abschnitt Aktionen auf ein Aktionstag seinen Aktionen zuzuordnen. Zeilen im Abschnitt Aktionen auch eine Zelle TagName, und die Zeilen mit denselben Zelle TagName-Wert wie diese Zelle Aktionen an, die für diese Aktionstag definieren. 
  
Zum Abrufen eines Verweises auf die Zelle TagName nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SmartTags.  *Name* . TagName wobei SmartTags. *Name* ist der Name der Zeile Aktionstag  <br/> |
   
Wenn Sie einen Verweis auf die Zelle TagName aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**VisRowSmartTag** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagName** <br/> |
   

