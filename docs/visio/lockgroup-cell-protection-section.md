---
title: Zelle "LockGroup" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
ms.localizationpriority: medium
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: Sperrt eine Gruppe, damit die Gruppierung nicht aufgehoben werden kann.
ms.openlocfilehash: cdb251fb66e522d2b2200f324b63410d9e83be1c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612498"
---
# <a name="lockgroup-cell-protection-section"></a>Zelle "LockGroup" (Abschnitt "Protection")

Sperrt eine Gruppe, damit die Gruppierung nicht aufgehoben werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Gruppierung der Gruppe kann nicht aufgehoben werden.  <br/> |
|FALSE  <br/> |Gruppierung der Gruppe kann aufgehoben werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie den Wert für LockGroupCell auf TRUE festlegen, wird auch das Löschen von Shapes verhindert, die Mitglieder der Gruppe sind.
  
Um einen Verweis auf die Zelle "LockGroup" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LockGroup  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockGroup anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLock** <br/> |
|Zellenindex:  <br/> |**visLockGroup** <br/> |
   

