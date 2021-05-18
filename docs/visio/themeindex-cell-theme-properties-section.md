---
title: Zelle "ThemeIndex" (Abschnitt "Theme Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Speichert die Aufzählung des integrierten Microsoft Visio, das auf das Dokument angewendet wurde, als ganze Zahl. Wenn ein neues Design für das Dokument ausgewählt wird, wird die Zelle ThemeIndex für das Dokument und alle seiten und Formen, die es enthält, mit dem Index des integrierten Designs aktualisiert.
ms.openlocfilehash: 6ddede864a54fbd7127552499d3ee1ae3d36efc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411911"
---
# <a name="themeindex-cell-theme-properties-section"></a>Zelle "ThemeIndex" (Abschnitt "Theme Properties")

Speichert die Aufzählung des integrierten Microsoft Visio, das auf das Dokument angewendet wurde, als ganze Zahl. Wenn ein neues Design für das Dokument ausgewählt wird, wird die **Zelle ThemeIndex** für das Dokument und alle seiten und Formen, die es enthält, mit dem Index des integrierten Designs aktualisiert. 
  
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **ThemeIndex-Zelle** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ThemeIndex  <br/> |
   
Um einen Verweis auf die **ThemeIndex-Zelle** nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowThemeProperties** <br/> |
| Zellenindex:  <br/> |**visThemeIndex** <br/> |
   

