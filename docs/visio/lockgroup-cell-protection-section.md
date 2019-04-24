---
title: Zelle "LockGroup" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
localization_priority: Normal
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: Sperrt eine Gruppe, damit die Gruppierung nicht aufgehoben werden kann.
ms.openlocfilehash: 0cb2c0653780dcb653e5903faaaa0ebf30ea9d69
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341792"
---
# <a name="lockgroup-cell-protection-section"></a>Zelle "LockGroup" (Abschnitt "Protection")

Sperrt eine Gruppe, damit die Gruppierung nicht aufgehoben werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Gruppierung der Gruppe kann nicht aufgehoben werden.  <br/> |
|FALSE  <br/> |Gruppierung der Gruppe kann aufgehoben werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie den Wert für LockGroupCell auf TRUE festlegen, wird auch das Löschen von Shapes verhindert, die Mitglieder der Gruppe sind.
  
Wenn Sie einen Verweis auf die Zelle LockGroup aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle LockGroup  <br/> |
   
Wenn Sie einen Verweis auf die Zelle LockGroup nach Index aus einem Programm abrufen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLock** <br/> |
|Zellenindex:  <br/> |**visLockGroup** <br/> |
   

