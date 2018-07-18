---
title: ThemeIndex Cell (Theme Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Speichert die Aufzählung des integrierten Microsoft Visio Design auf das Dokument, als ganze Zahl. Wenn ein neues Design für das Dokument ausgewählt ist, wird die Zelle ThemeIndex für das Dokument und alle Seiten und Shapes darin enthaltenen mit dem Index des integrierten Designs aktualisiert.
ms.openlocfilehash: 8a9202631bc4d9131d52dea1f852983e1d7528e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798259"
---
# <a name="themeindex-cell-theme-properties-section"></a>ThemeIndex Cell (Theme Properties Section)

Speichert die Aufzählung des integrierten Microsoft Visio Design auf das Dokument, als ganze Zahl. Wenn ein neues Design für das Dokument, das die Zelle **ThemeIndex** für das Dokument ausgewählt ist, und alle Seiten und die darin enthaltenen Shapes wird mit dem Index des integrierten Designs aktualisiert. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **ThemeIndex** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ThemeIndex  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **ThemeIndex** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowThemeProperties** <br/> |
| Zellenindex:  <br/> |**visThemeIndex** <br/> |
   

