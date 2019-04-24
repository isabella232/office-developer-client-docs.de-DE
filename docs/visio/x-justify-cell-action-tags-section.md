---
title: Zelle "X Justify" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
localization_priority: Normal
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: Der x-Offset der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist.
ms.openlocfilehash: f8542d2f3a22b12794d999323d202d7a5bece20b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284972"
---
# <a name="x-justify-cell-action-tags-section"></a>Zelle "X Justify" (Abschnitt "Action Tags")

Der *x* -Offset der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Links ausgerichtet (Standard).  <br/> |**visSmartTagXJustifyLeft** <br/> |
| 1  <br/> | Zentriert.  <br/> |**visSmartTagXJustifyCenter** <br/> |
| 2  <br/> | Rechts ausgerichtet.  <br/> |**visSmartTagXJustifyRight** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Zellen X Blocksatz und Y-Ausrichtung legen fest, wo die Schaltfläche Aktionstag in Bezug auf den in den Zellen X und Y definierten Punkt angeordnet wird. 
  
Wenn Sie einen Verweis auf die Zelle X Blocksatz aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Smarttags.  *Name* . XJustify, wobei SmartTags. *Name* ist der Name der Zeile mit dem Aktionstag.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle X Blocksatz aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**visRowSmartTag** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagXJustify** <br/> |
   

