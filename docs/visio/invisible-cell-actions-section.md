---
title: Zelle "Invisible" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60046
localization_priority: Normal
ms.assetid: 070b4468-c907-b201-1633-1d3e10ecc2b2
description: Zeigt an, ob die Aktion im Aktionstag- oder Kontextmenü sichtbar ist.
ms.openlocfilehash: 69bc96e76f27a64d6e1443f045c27566f598c1db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297242"
---
# <a name="invisible-cell-actions-section"></a>Zelle "Invisible" (Abschnitt "Actions")

Zeigt an, ob die Aktion im Aktionstag- oder Kontextmenü sichtbar ist. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die Aktion ist nicht im Menü sichtbar.  <br/> |
|FALSE  <br/> |Die Aktion ist im Menü sichtbar (Standard).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle inVisible aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name* . Invisiblewobei-Aktionen.  *Name* ist der Name der Zeile Actions.  <br/> |
   
Wenn Sie einen Verweis auf die unsichtbare Zelle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionInvisible** <br/> |
   

