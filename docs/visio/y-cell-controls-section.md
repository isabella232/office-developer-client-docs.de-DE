---
title: Zelle "Y" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251282
localization_priority: Normal
ms.assetid: dd7ea5fa-1d34-44e8-5a29-69ca542aecba
description: Stellt die y-Koordinate, die die Position des Steuerpunkts in lokalen Koordinaten des Shapes anzeigt.
ms.openlocfilehash: 8104ae6d647feb4e1b83474b63f40e243e5405e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798453"
---
# <a name="y-cell-controls-section"></a>Zelle "Y" (Abschnitt "Controls")

Stellt die *y* -Koordinate, die die Position des Steuerpunkts in lokalen Koordinaten des Shapes anzeigt. 
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle Y nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name* . Ywhere-Steuerelemente.  *Name* ist der Name der Zeile mit Steuerelementen.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Y aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionControls** <br/> |
| Zeilenindex:  <br/> |**VisRowControl** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCtlY** <br/> |
   

