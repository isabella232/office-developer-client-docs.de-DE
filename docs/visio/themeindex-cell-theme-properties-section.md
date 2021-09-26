---
title: Zelle "ThemeIndex" (Abschnitt "Theme Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Speichert die Aufzählung des integrierten Microsoft Visio Designs, das auf das Dokument angewendet wird, als ganze Zahl. Wenn ein neues Design für das Dokument ausgewählt wird, wird die Zelle ThemeIndex für das Dokument sowie alle darin enthaltenen Seiten und Formen mit dem Index des integrierten Designs aktualisiert.
ms.openlocfilehash: a016fdef87fd0324b71cb912482fa9f1d797b946
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603305"
---
# <a name="themeindex-cell-theme-properties-section"></a>Zelle "ThemeIndex" (Abschnitt "Theme Properties")

Speichert die Aufzählung des integrierten Microsoft Visio Designs, das auf das Dokument angewendet wird, als ganze Zahl. Wenn ein neues Design für das Dokument ausgewählt wird, wird die Zelle **ThemeIndex** für das Dokument sowie alle darin enthaltenen Seiten und Formen mit dem Index des integrierten Designs aktualisiert. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die **Zelle ThemeIndex** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ThemeIndex  <br/> |
   
Um einen Verweis auf die Zelle **ThemeIndex** anhand des Indexes aus einem Programm abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowThemeProperties** <br/> |
| Zellenindex:  <br/> |**visThemeIndex** <br/> |
   

