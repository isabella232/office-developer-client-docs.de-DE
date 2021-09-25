---
title: Zelle "ButtonFace" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60026
ms.localizationpriority: medium
ms.assetid: 26f370e1-5193-f47d-7b60-3597975be650
description: Enthält die ID der Schaltflächenoberseite, die auf der Schaltfläche Aktionstag angezeigt wird.
ms.openlocfilehash: b445a35fe6582b07fd988eacec24725d36466aca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578130"
---
# <a name="buttonface-cell-action-tags-section"></a>Zelle "ButtonFace" (Abschnitt "Action Tags")

Enthält die ID der Schaltflächenoberseite, die auf der Schaltfläche Aktionstag angezeigt wird. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Zeichenfolge in einer ButtonFace-Zelle stellt die ID einer Microsoft Office-Schaltflächenoberseite dar. Der Wert 0 (Null) oder leerer Standardwert für die Standardmäßige Aktionstag-Infoschaltfläche "i" ![Standard-Aktionstag -Infoschaltfläche "i"](media/InfoPS_ZA10180114.gif).
  
Die IDs, die in der Zelle ButtonFace verwendet werden können, entsprechen den IDs, die mit der **FaceID-Eigenschaft** eines **CommandBarButton-Objekts** verwendet werden. Weitere Informationen zu diesen IDs erhalten Sie, indem Sie auf MSDN nach "Arbeiten mit Befehlsleisten-Schaltflächenbildern" suchen. 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "ButtonFace" anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SmartTags.  *Name*  . ButtonFace where SmartTags. *Name*  ist der Name der Aktionstagzeile  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ButtonFace anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**visRowSmartTag**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagButtonFace** <br/> |
   

