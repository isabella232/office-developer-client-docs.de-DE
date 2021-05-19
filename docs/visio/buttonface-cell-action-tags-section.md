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
  
## <a name="remarks"></a>Hinweise

Die Zeichenfolge in einer ButtonFace-Zelle stellt die ID einer Microsoft Office-Schaltflächenoberseite dar. Der Wert 0 (Null) oder leer ist standardmäßig auf die Standard-Aktionstag-Infoschaltfläche "i" festgelegt. ![Standardaktionstag "i"-Infoschaltfläche](media/InfoPS_ZA10180114.gif).
  
Die IDs, die in der Zelle ButtonFace verwendet werden können, sind identisch mit den IDs, die mit der **FaceID-Eigenschaft** eines **CommandBarButton-Objekts verwendet** werden. Weitere Informationen zu diesen IDs finden Sie unter "Arbeiten mit Befehlsleistenschaltflächebildern" auf MSDN. 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle ButtonFace anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SmartTags.  *Name*  . ButtonFace, wo SmartTags. *Name*  ist der Name der Aktionstagzeile  <br/> |
   
Um einen Verweis auf die ButtonFace-Zelle nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**visRowSmartTag**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagButtonFace** <br/> |
   

