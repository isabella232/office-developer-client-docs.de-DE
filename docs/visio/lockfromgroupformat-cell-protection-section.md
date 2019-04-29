---
title: Zelle "LockFromGroupFormat" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 3daeb4704a33ba836cf82c9ab3517c6ca6be8db7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426058"
---
# <a name="lockfromgroupformat-cell-protection-section"></a>Zelle "LockFromGroupFormat" (Abschnitt "Protection")

Blockiert Formatänderungen an einem Gruppen-Shape, die an die unter Formen weitergegeben werden, während Benutzer die ausgewählten unter Formen weiterhin direkt formatieren können. 
  
Der Wert der Zelle LockFromGroupFormat entspricht dem Kontrollkästchen **von Gruppen Formatierungen** im Dialogfeld **Schutz** . 
  
Wenn Sie auf die Zelle LockFromGroupFormat aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen verweisen möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LockFromGroupFormat  <br/> |
   
Wenn Sie aus einem Programm aus nach Index auf die Zelle LockFromGroupFormat verweisen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLock** <br/> |
|Zellenindex:  <br/> |**visLockFromGroupFormat** <br/> |
   
Der Standardwert für diese Zelle ist 0 (False).
  

