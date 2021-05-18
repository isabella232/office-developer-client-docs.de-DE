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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412716"
---
# <a name="tagname-cell-actions-section"></a>Zelle "TagName" (Abschnitt "Actions")

Enthält den Namen des Aktionstags, mit dem diese Aktion verknüpft ist.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>Hinweise

Über die Zellen TagName im Abschnitt Actions und im Abschnitt Action Tags erfolgt das Zuordnen eines Aktionstags zu den damit verknüpften Aktionen. 
  
- Wenn die Zelle TagName in einer Actions-Zeile leer ist, wird die Aktion in einem Kontextmenü und nicht in einem Aktionstagmenü angezeigt.
    
- Wenn ein TagName-Zellwert in der Zeile Aktionen mit dem TagName-Zellwert in einer SmartTags-Zeile entspricht, wird die Aktion im Menü Aktionstag angezeigt.
    
- Wenn die TagName-Zelle einer Aktion über einen Wert verfügt, sie jedoch nicht mit dem TagName-Wert in einer Shape-Tag-Zeile übereinstimmen, wird diese Aktion nicht in Aktionstagmenüs oder Kontextmenüs angezeigt.
    
- Wenn mehrere Smarttag-Zeilen den gleichen Wert in der Zelle TagName aufweisen, wird überall die gleiche Aktion angezeigt.
    
Um einen Verweis auf die TagName-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name*  . TagNamewhere-Aktionen.  *Name*  ist der Name der Zeile Aktionen  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die TagName-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionTagName** <br/> |
   

