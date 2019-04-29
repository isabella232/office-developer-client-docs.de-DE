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
description: Stellt die y-Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten angibt.
ms.openlocfilehash: 14aaa7aef7e7250baeb8ffb863244ece26a201e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407949"
---
# <a name="y-cell-controls-section"></a>Zelle "Y" (Abschnitt "Controls")

Stellt die *y* -Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten angibt. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Y aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name* . Ywobei-Steuerelemente.  *Name* ist der Name der Zeile Controls.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Y nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionControls** <br/> |
| Zeilenindex:  <br/> |**visRowControl** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCtlY** <br/> |
   

