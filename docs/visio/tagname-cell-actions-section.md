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
ms.openlocfilehash: e1495a34769cbcfdd687491855d1f9c761de2b4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798242"
---
# <a name="tagname-cell-actions-section"></a>Zelle "TagName" (Abschnitt "Actions")

Enthält den Namen des Aktionstags, mit dem diese Aktion verknüpft ist.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>Bemerkungen

Über die Zellen TagName im Abschnitt Actions und im Abschnitt Action Tags erfolgt das Zuordnen eines Aktionstags zu den damit verknüpften Aktionen. 
  
- Wenn in der Zeile Actions die Zelle TagName leer ist, wird die Aktion im Kontextmenü, nicht auf eine im Aktionstagmenü angezeigt.
    
- Wenn ein Zellwert TagName in der Zeile Actions der Wert der TagName Zelle in einer Zeile Smart Tags entspricht, wird die Aktion auf im Aktionstagmenü angezeigt.
    
- Zelle "TagName" eine Aktion verfügt über einen Wert, jedoch entspricht nicht den Wert in einer beliebigen Form-Tag-Zeile, wird diese Aktion nicht auf eine beliebige Aktionstag oder Kontextmenüs angezeigt.
    
- Wenn mehrere Smarttag-Zeilen den gleichen Wert in der Zelle TagName aufweisen, wird überall die gleiche Aktion angezeigt.
    
Wenn Sie einen Verweis auf die Zelle TagName nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name* . TagNamewhere Aktionen.  *Name* ist der Name der Zeile Actions  <br/> |
   
Wenn Sie einen Verweis auf die Zelle TagName aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**VisRowAction** +  *i* wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionTagName** <br/> |
   

