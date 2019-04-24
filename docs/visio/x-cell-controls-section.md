---
title: Zelle "X" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251281
localization_priority: Normal
ms.assetid: b7aea554-f491-6a9a-4d07-feeab739a9df
description: Stellt die x-Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten angibt.
ms.openlocfilehash: 58eea4e9c3cfe127c4adcc7fb75e395f53874dd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269783"
---
# <a name="x-cell-controls-section"></a>Zelle "X" (Abschnitt "Controls")

Stellt die *x* -Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten angibt. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle X aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name* . X, wobei Steuerelemente.  *Name* ist der Name der Zeile Controls.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle X aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionControls** <br/> |
| Zeilenindex:  <br/> |**visRowControl** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCtlX** <br/> |
   

