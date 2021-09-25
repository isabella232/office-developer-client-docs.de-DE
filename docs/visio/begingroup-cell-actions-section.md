---
title: Zelle "BeginGroup" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
ms.localizationpriority: medium
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: Gibt an, ob über dieser Aktion ein Trennzeichen in das Menü eingefügt wird.
ms.openlocfilehash: 7f6ce3836cf71adcdb7135c390abc84834d57fad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616026"
---
# <a name="begingroup-cell-actions-section"></a>Zelle "BeginGroup" (Abschnitt "Actions")

Gibt an, ob über dieser Aktion ein Trennzeichen in das Menü eingefügt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Über der Aktion wird ein Trennzeichen in das Menü eingefügt.  <br/> |
|FALSE  <br/> |Über der Aktion wird kein Trennzeichen in das Menü eingefügt (Standard).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um einen Verweis auf die Zelle "BeginGroup" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name*. BeginGroup where Actions. *Name* ist der Name der Zeile "Aktionen"  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle BeginGroup anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionBeginGroup** <br/> |
   

