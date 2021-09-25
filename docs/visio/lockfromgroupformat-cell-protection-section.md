---
title: Zelle "LockFromGroupFormat" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: ef4cd97298108f64f4fdc7fcd5d690bfeeb16bbc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554446"
---
# <a name="lockfromgroupformat-cell-protection-section"></a>Zelle "LockFromGroupFormat" (Abschnitt "Protection")

Verhindert, dass Formatänderungen an einem Gruppen-Shape an seine Untergeordneten Shapes weitergegeben werden, während Benutzer weiterhin ausgewählte Unterformen direkt formatieren können. 
  
Der Wert der Zelle LockFromGroupFormat entspricht der Einstellung des Kontrollkästchens für die Formatierung von **Gruppen** im Dialogfeld Schutz.  
  
To refer to the LockFromGroupFormat cell by name from another formula, or from a program, using the **CellsU** property, use: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LockFromGroupFormat  <br/> |
   
To refer to the LockFromGroupFormat cell by index from a program, use the **CellsSRC** property with the following arguments: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLock** <br/> |
|Zellenindex:  <br/> |**visLockFromGroupFormat** <br/> |
   
Der Standardwert für diese Zelle ist 0 (False).
  

