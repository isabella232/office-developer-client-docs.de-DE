---
title: Zelle "Invisible" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60046
ms.localizationpriority: medium
ms.assetid: 070b4468-c907-b201-1633-1d3e10ecc2b2
description: Zeigt an, ob die Aktion im Aktionstag- oder Kontextmenü sichtbar ist.
ms.openlocfilehash: ffc213fd19b3a39e644ddea57bbe99dc367bbeab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598528"
---
# <a name="invisible-cell-actions-section"></a>Zelle "Invisible" (Abschnitt "Actions")

Zeigt an, ob die Aktion im Aktionstag- oder Kontextmenü sichtbar ist. 
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die Aktion ist nicht im Menü sichtbar.  <br/> |
|FALSE  <br/> |Die Aktion ist im Menü sichtbar (Standard).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle "Invisible" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name*  . InvisibleWhere-Aktionen.  *Name*  ist der Name der Zeile "Aktionen"  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "Invisible" anhand des Indexes aus einem Programm abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionInvisible** <br/> |
   

