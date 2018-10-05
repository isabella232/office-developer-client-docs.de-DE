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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385480"
---
# <a name="buttonface-cell-action-tags-section"></a>ButtonFace Cell (Action Tags Section)

Enthält die ID der Schaltflächenoberseite, die auf der Schaltfläche Aktionstag angezeigt wird. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>Hinweise

Die Zeichenfolge in einer ButtonFace-Zelle stellt die ID einer Microsoft Office-Schaltflächenoberseite dar. Der Wert 0 (Null) oder kein Eintrag ergibt die Standardaktionstag-Infoschaltfläche "i" ![Standard Aktionstag "i" Info-Schaltfläche](media/InfoPS_ZA10180114.gif).
  
Die IDs, die in die Zelle ButtonFace verwendet werden können, sind identisch mit den IDs, die mit der **FaceID** -Eigenschaft eines **CommandBarButton** -Objekts. Weitere Informationen zu diesen IDs auf MSDN nach "Working with Schaltflächensymbolen an Leiste Befehl" suchen. 
  
Wenn Sie einen Verweis auf die Zelle ButtonFace aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SmartTags.  *Name* . ButtonFace wobei SmartTags. *Name* ist der Name der Zeile Aktionstag  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ButtonFace aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**VisRowSmartTag** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagButtonFace** <br/> |
   

