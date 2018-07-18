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
ms.openlocfilehash: 749f611209d362811f5e4fb051780a4a642295c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796425"
---
# <a name="begingroup-cell-actions-section"></a>BeginGroup Cell (Actions Section)

Gibt an, ob über dieser Aktion ein Trennzeichen in das Menü eingefügt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |
          Über der Aktion wird ein Trennzeichen in das Menü eingefügt. 
  <br/> |
|FALSE  <br/> |
          Über der Aktion wird kein Trennzeichen in das Menü eingefügt (Standard).
  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle BeginGroup aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name*. BeginGroup wobei Aktionen. *Name* ist der Name der Zeile Actions  <br/> |
   
Wenn Sie einen Verweis auf die Zelle BeginGroup aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**VisRowAction** +  *i* wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionBeginGroup** <br/> |
   

