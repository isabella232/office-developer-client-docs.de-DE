---
title: QuickStyleFontColor Cell (Quick Style section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: Bestimmt die Schriftfarbe aus den Schnellformatvorlagen, die der Text eines Shapes vom aktiven Design erbt, als ganze Zahl von 0-1.
ms.openlocfilehash: bd645383df02260fcf6a2045764d9a1b44126090
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282635"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a>QuickStyleFontColor Cell (Quick Style section)

Bestimmt die Schriftfarbe aus den Schnellformatvorlagen, die der Text eines Shapes vom aktiven Design erbt, als ganze Zahl von 0-1. 
  
|||
|:-----|:-----|
|Wert  <br/> |Beschreibung  <br/> |
|0  <br/> |Der Shape-Text verwendet die dunkle Schriftfarbe.  <br/> |
|1  <br/> |Der Shape-Text verwendet die Schriftfarbe Light.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **QuickStyleFontColor** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | QuickStyleFontColor  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **QuickStyleFontColor** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
| Zellenindex:  <br/> |**visQuickStyleFontColor** <br/> |
   

