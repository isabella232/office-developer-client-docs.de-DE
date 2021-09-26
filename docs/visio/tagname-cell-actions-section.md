---
title: Zelle "TagName" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60087
ms.localizationpriority: medium
ms.assetid: e593e95d-f975-481d-69cd-619049d4427d
description: Enthält den Namen des Aktionstags, mit dem diese Aktion verknüpft ist.
ms.openlocfilehash: 597becdd03d7cc52222b48335b676f7b57b4df43
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627358"
---
# <a name="tagname-cell-actions-section"></a>Zelle "TagName" (Abschnitt "Actions")

Enthält den Namen des Aktionstags, mit dem diese Aktion verknüpft ist.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>Bemerkungen

Über die Zellen TagName im Abschnitt Actions und im Abschnitt Action Tags erfolgt das Zuordnen eines Aktionstags zu den damit verknüpften Aktionen. 
  
- Wenn die Zelle TagName in einer Zeile Aktionen leer ist, wird die Aktion in einem Kontextmenü und nicht in einem Aktionstagmenü angezeigt.
    
- Wenn ein TagName-Zellenwert in der Zeile Actions mit dem Wert der Zelle TagName in einer SmartTag-Zeile übereinstimmt, wird die Aktion im Aktionstagmenü angezeigt.
    
- Wenn die Zelle TagName einer Aktion einen Wert aufweist, jedoch nicht mit dem TagName-Wert in einer Shape-Tag-Zeile übereinstimmt, wird diese Aktion nicht in Aktionstagmenüs oder Kontextmenüs angezeigt.
    
- Wenn mehrere Smarttag-Zeilen den gleichen Wert in der Zelle TagName aufweisen, wird überall die gleiche Aktion angezeigt.
    
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "TagName" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name*  . TagNamewhere Actions.  *Name*  ist der Name der Zeile "Aktionen"  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle TagName anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionTagName** <br/> |
   

