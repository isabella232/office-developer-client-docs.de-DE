---
title: Zelle "TagName" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60087
localization_priority: Normal
ms.assetid: e593e95d-f975-481d-69cd-619049d4427d
description: Enthält den Namen des Aktionstags, mit dem diese Aktion verknüpft ist.
ms.openlocfilehash: e7bf5db940934d168ac2adb86d05b0374b0fd265
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332389"
---
# <a name="tagname-cell-actions-section"></a>Zelle "TagName" (Abschnitt "Actions")

Enthält den Namen des Aktionstags, mit dem diese Aktion verknüpft ist.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>Bemerkungen

Über die Zellen TagName im Abschnitt Actions und im Abschnitt Action Tags erfolgt das Zuordnen eines Aktionstags zu den damit verknüpften Aktionen. 
  
- Wenn die Zelle TagName in einer Zeile Aktionen leer ist, wird die Aktion in einem Kontextmenü und nicht in einem aktionstagmenü angezeigt.
    
- Wenn der Zellenwert TagName in der Zeile Actions mit dem Zellenwert TagName in einer Smarttag-Zeile übereinstimmt, wird die Aktion im Menü Aktionstag angezeigt.
    
- Wenn die Zelle TagName einer Aktion einen Wert aufweist, aber nicht mit dem Wert TagName in einer beliebigen Shape-Tag-Zeile übereinstimmt, wird diese Aktion nicht in einem Aktionstag-oder Kontextmenü angezeigt.
    
- Wenn mehrere Smarttag-Zeilen den gleichen Wert in der Zelle TagName aufweisen, wird überall die gleiche Aktion angezeigt.
    
Wenn Sie einen Verweis auf die Zelle TagName aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name* . Tagnamewobei-Aktionen.  *Name* ist der Name der Zeile Actions.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle TagName aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionTagName** <br/> |
   

