---
title: Zelle "BeginGroup" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
localization_priority: Normal
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: Gibt an, ob über dieser Aktion ein Trennzeichen in das Menü eingefügt wird.
ms.openlocfilehash: 115dbfe051201dc3ec2b127ff129b077e1067865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361033"
---
# <a name="begingroup-cell-actions-section"></a>Zelle "BeginGroup" (Abschnitt "Actions")

Gibt an, ob über dieser Aktion ein Trennzeichen in das Menü eingefügt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Über der Aktion wird ein Trennzeichen in das Menü eingefügt.  <br/> |
|FALSE  <br/> |Über der Aktion wird kein Trennzeichen in das Menü eingefügt (Standard).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle beginGroup aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name*. BeginGroup-Aktion. *Name* ist der Name der Zeile Actions.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle beginGroup nach Index aus einem Programm abrufen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionBeginGroup** <br/> |
   

