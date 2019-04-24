---
title: ThemeIndex Cell (Theme Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Speichert die Enumeration des integrierten Microsoft Visio-Designs, das auf das Dokument angewendet wird, als ganze Zahl. Wenn ein neues Design für das Dokument ausgewählt wird, wird die ThemeIndex-Zelle für das Dokument und alle darin enthaltenen Seiten und Formen mit dem Index des integrierten Designs aktualisiert.
ms.openlocfilehash: 6ddede864a54fbd7127552499d3ee1ae3d36efc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360529"
---
# <a name="themeindex-cell-theme-properties-section"></a>ThemeIndex Cell (Theme Properties section)

Speichert die Enumeration des integrierten Microsoft Visio-Designs, das auf das Dokument angewendet wird, als ganze Zahl. Wenn ein neues Design für das Dokument ausgewählt wird, wird die **ThemeIndex** -Zelle für das Dokument und alle darin enthaltenen Seiten und Formen mit dem Index des integrierten Designs aktualisiert. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **ThemeIndex** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ThemeIndex  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **ThemeIndex** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowThemeProperties** <br/> |
| Zellenindex:  <br/> |**visThemeIndex** <br/> |
   

