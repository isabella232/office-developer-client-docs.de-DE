---
title: Zelle "LockThemeColors" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70001
localization_priority: Normal
ms.assetid: 22cedeb3-58b5-3932-9252-5c9dd3e163e3
ms.openlocfilehash: 2ca8af2c7a41259af73a111af331ce1031e5f46c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19797398"
---
# <a name="lockthemecolors-cell-protection-section"></a>LockThemeColors Cell (Protection Section)

Verhindert, dass Designfarben auf das Shape angewendet werden. 
  
Der Wert der Zelle LockThemeColors entspricht der Einstellung für das Kontrollkästchen **von Designfarben** im Dialogfeld **Schutz** . 
  
Auf die Zelle LockThemeColors aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen verweisen verwenden: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LockThemeColors  <br/> |
   
Wenn Sie auf die Zelle LockThemeColors durch Index aus einem Programm verweisen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLock** <br/> |
|Zellenindex:  <br/> |**visLockThemeColors** <br/> |
   

