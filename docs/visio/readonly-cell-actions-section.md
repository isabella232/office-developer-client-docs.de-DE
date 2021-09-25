---
title: Zelle "ReadOnly" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60071
ms.localizationpriority: medium
ms.assetid: 158b4188-570c-3817-bf34-8dc0c64befa5
description: Steuert, ob die Aktion in einem Aktionstag- oder Kontextmenü schreibgeschützt ist.
ms.openlocfilehash: af4a2d4945032a100d39440c9c3bed427d310c06
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559738"
---
# <a name="readonly-cell-actions-section"></a>Zelle "ReadOnly" (Abschnitt "Actions")

Steuert, ob die Aktion in einem Aktionstag- oder Kontextmenü schreibgeschützt ist. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die Aktion wird im Menü angezeigt, ist aber schreibgeschützt.  <br/> |
|FALSE  <br/> |Die Aktion wird im Menü angezeigt und kann ausgewählt werden (Standardeinstellung).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn eine Aktion schreibgeschützt ist, wird sie im Aktionstag- oder Kontextmenü angezeigt, kann jedoch nicht ausgewählt werden. Sie ist nicht grau unterlegt, wird aber wie eine Beschriftung vor einem farbigen Hintergrund angezeigt. Wenn Sie das Menüelement grau unterlegt anzeigen lassen möchten, verwenden Sie die Zelle Disabled. 
  
Um einen Verweis auf die Zelle "ReadOnly" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name*  . ReadOnlywhere-Aktionen.  *Name*  ist der Name der Zeile "Aktionen"  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ReadOnly anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionReadOnly** <br/> |
   

