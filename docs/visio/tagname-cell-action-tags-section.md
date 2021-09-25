---
title: Zelle "TagName" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
ms.localizationpriority: medium
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: Der Name des Aktionstags, das als Schlüssel verwendet wird, um das Aktionstag seinen Aktionen zuzuordnen.
ms.openlocfilehash: 09bd43f69e1adb757ab71e34b232f79affa10e2d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622753"
---
# <a name="tagname-cell-action-tags-section"></a>Zelle "TagName" (Abschnitt "Action Tags")

Der Name des Aktionstags, das als Schlüssel verwendet wird, um das Aktionstag seinen Aktionen zuzuordnen.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>Bemerkungen

 Die Zelle TagName im Abschnitt Action Tags arbeitet mit der Zelle TagName im Abschnitt Actions zusammen, um ein Aktionstag ihren Aktionen zuzuordnen. Zeilen im Abschnitt Actions besitzen auch eine Zelle TagName, und diese Zeilen mit demselben TagName-Zellwert wie diese Zelle definieren Aktionen, die für dieses Aktionstag ausgeführt werden sollen. 
  
Um einen Verweis auf die Zelle TagName anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SmartTags.  *Name*  . TagName where SmartTags. *Name*  ist der Name der Aktionstagzeile  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle TagName anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**visRowSmartTag**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagName** <br/> |
   

