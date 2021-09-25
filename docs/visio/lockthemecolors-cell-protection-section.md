---
title: Zelle "LockThemeColors" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70001
ms.localizationpriority: medium
ms.assetid: 22cedeb3-58b5-3932-9252-5c9dd3e163e3
ms.openlocfilehash: e4a96cab2939c17980a7f0daba6af65ddcac4045
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623376"
---
# <a name="lockthemecolors-cell-protection-section"></a>Zelle "LockThemeColors" (Abschnitt "Protection")

Verhindert die Anwendung von Designfarben auf das Shape. 
  
Der Wert der Zelle LockThemeColors entspricht der Einstellung des Kontrollkästchens **"Von Designfarben"** im Dialogfeld Schutz.  
  
To refer to the LockThemeColors cell by name from another formula, or from a program, using the **CellsU** property, use: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LockThemeColors  <br/> |
   
To refer to the LockThemeColors cell by index from a program, use the **CellsSRC** property with the following arguments: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLock** <br/> |
|Zellenindex:  <br/> |**visLockThemeColors** <br/> |
   

