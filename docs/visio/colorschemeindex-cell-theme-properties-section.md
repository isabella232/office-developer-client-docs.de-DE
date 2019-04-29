---
title: ColorSchemeIndex Cell (Theme Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb84f71e-59c4-43d4-a28b-c3d6f267d2ae
description: Bestimmt den Index des Designs, nach dem das Farbschema des Shapes stattfindet, als ganze Zahl.
ms.openlocfilehash: d67363b48454a717914b8ff9e39952609d848118
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430763"
---
# <a name="colorschemeindex-cell-theme-properties-section"></a>ColorSchemeIndex Cell (Theme Properties section)

Bestimmt den Index des Designs, nach dem das Farbschema des Shapes stattfindet, als ganze Zahl.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **ColorSchemeIndex** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ColorSchemeIndex  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **ColorSchemeIndex** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowThemeProperties** <br/> |
| Zellenindex:  <br/> |**visColorSchemeIndex** <br/> |
   

