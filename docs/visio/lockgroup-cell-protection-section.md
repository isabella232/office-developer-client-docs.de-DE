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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404309"
---
# <a name="lockgroup-cell-protection-section"></a>Zelle "LockGroup" (Abschnitt "Protection")

Sperrt eine Gruppe, damit die Gruppierung nicht aufgehoben werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Gruppierung der Gruppe kann nicht aufgehoben werden.  <br/> |
|FALSE  <br/> |Gruppierung der Gruppe kann aufgehoben werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie den Wert für LockGroupCell auf TRUE festlegen, wird auch das Löschen von Shapes verhindert, die Mitglieder der Gruppe sind.
  
Um einen Verweis auf die Zelle LockGroup anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LockGroup  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockGroup nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLock** <br/> |
|Zellenindex:  <br/> |**visLockGroup** <br/> |
   

