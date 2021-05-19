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
ms.openlocfilehash: 777d6c1098888c9835c1ad367bb70926b835180b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417910"
---
# <a name="tagname-cell-action-tags-section"></a>Zelle "TagName" (Abschnitt "Action Tags")

Der Name des Aktionstags, das als Schlüssel verwendet wird, um das Aktionstag seinen Aktionen zuzuordnen.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>Hinweise

 Die Zelle TagName im Abschnitt Aktionstags arbeitet mit der Zelle TagName im Abschnitt Aktionen zusammen, um den Aktionen ein Aktionstag zuzuordnen. Zeilen im Abschnitt Aktionen haben auch eine TagName-Zelle, und diese Zeilen mit demselben TagName-Zellwert wie diese Zelle definieren Aktionen, die für dieses Aktionstag zu ergreifen sind. 
  
Um einen Verweis auf die TagName-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SmartTags.  *Name*  . TagName, wobei SmartTags. *Name*  ist der Name der Aktionstagzeile  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die TagName-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**visRowSmartTag**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagName** <br/> |
   

