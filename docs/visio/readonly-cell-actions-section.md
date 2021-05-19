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
ms.openlocfilehash: f45f22001a4d7275bb9367414c8b04ea3c0d9c6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434235"
---
# <a name="readonly-cell-actions-section"></a>Zelle "ReadOnly" (Abschnitt "Actions")

Steuert, ob die Aktion in einem Aktionstag- oder Kontextmenü schreibgeschützt ist. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die Aktion wird im Menü angezeigt, ist aber schreibgeschützt.  <br/> |
|FALSE  <br/> |Die Aktion wird im Menü angezeigt und kann ausgewählt werden (Standardeinstellung).  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn eine Aktion schreibgeschützt ist, wird sie im Aktionstag- oder Kontextmenü angezeigt, kann jedoch nicht ausgewählt werden. Sie ist nicht grau unterlegt, wird aber wie eine Beschriftung vor einem farbigen Hintergrund angezeigt. Wenn Sie das Menüelement grau unterlegt anzeigen lassen möchten, verwenden Sie die Zelle Disabled. 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle ReadOnly anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name*  . ReadOnlywhere-Aktionen.  *Name*  ist der Name der Zeile Aktionen  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ReadOnly nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionReadOnly** <br/> |
   

