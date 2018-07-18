---
title: Zelle "ReadOnly" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60071
localization_priority: Normal
ms.assetid: 158b4188-570c-3817-bf34-8dc0c64befa5
description: Steuert, ob die Aktion in einem Aktionstag- oder Kontextmenü schreibgeschützt ist.
ms.openlocfilehash: bf2d0f7e50a3126611662af8e068485986c26a13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797768"
---
# <a name="readonly-cell-actions-section"></a>ReadOnly Cell (Actions Section)

Steuert, ob die Aktion in einem Aktionstag- oder Kontextmenü schreibgeschützt ist. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die Aktion wird im Menü angezeigt, ist aber schreibgeschützt.  <br/> |
|FALSE  <br/> |Die Aktion wird im Menü angezeigt und kann ausgewählt werden (Standardeinstellung).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn eine Aktion schreibgeschützt ist, wird auf das Aktionsmenü Aktionstag- oder Kontextmenü angezeigt, aber nicht ausgewählt werden. Es ist nicht abgeblendet, aber vielmehr auf einem farbigen Hintergrund, wie eine Beschriftung angezeigt wird. Damit das Menüelement abgeblendet angezeigt wird, verwenden Sie die Zelle Disabled aus. 
  
Wenn Sie einen Verweis auf die Zelle ReadOnly aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name* . ReadOnlywhere Aktionen.  *Name* ist der Name der Zeile Actions  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ReadOnly aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**VisRowAction** +  *i* wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionReadOnly** <br/> |
   

