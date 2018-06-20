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
description: Stellt die X-Koordinate, die die Position des Steuerpunkts in lokalen Koordinaten des Shapes anzeigt.
ms.openlocfilehash: e47b26c72709a2ee74675e73b8e8424bbfb325e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798433"
---
# <a name="x-cell-controls-section"></a>Zelle "X" (Abschnitt "Controls")

Stellt die *X* -Koordinate, die die Position des Steuerpunkts in lokalen Koordinaten des Shapes anzeigt. 
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle X nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name* . X Where steuert.  *Name* ist der Name der Zeile mit Steuerelementen.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle X aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionControls** <br/> |
| Zeilenindex:  <br/> |**VisRowControl** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCtlX** <br/> |
   

