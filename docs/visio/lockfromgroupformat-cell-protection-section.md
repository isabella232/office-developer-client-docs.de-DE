---
title: Zelle "LockFromGroupFormat" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 95633ab7a4127564fef65062bcf328d4364ebd86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19797391"
---
# <a name="lockfromgroupformat-cell-protection-section"></a>LockFromGroupFormat Cell (Protection Section)

Blöcke format, Änderungen in einem Gruppen-Shape aus, die Teil-Shapes weitergegeben wird, während Benutzer dennoch ausgewählten untergeordneten Shapes direkt zu formatieren. 
  
Der Wert der Zelle LockFromGroupFormat entspricht der Einstellung für das Kontrollkästchen **von gruppenformatierung** im Dialogfeld **Schutz** . 
  
Auf die Zelle LockFromGroupFormat aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen verweisen verwenden: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LockFromGroupFormat  <br/> |
   
Wenn Sie auf die Zelle LockFromGroupFormat durch Index aus einem Programm verweisen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLock** <br/> |
|Zellenindex:  <br/> |**visLockFromGroupFormat** <br/> |
   
Der Standardwert für diese Zelle ist 0 (False).
  

