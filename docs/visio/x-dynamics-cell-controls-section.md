---
title: Zelle "X Dynamics" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
localization_priority: Normal
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: Stellt die X-Koordinate für den Verankerungspunkt eines Steuerpunkts, in lokalen Koordinaten dar.
ms.openlocfilehash: 9dee2381c15ed2817df9f89ebc830cf31bf64c1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798457"
---
# <a name="x-dynamics-cell-controls-section"></a>X Dynamics Cell (Controls Section)

Stellt die *X* -Koordinate für den Verankerungspunkt eines Steuerpunkts, in lokalen Koordinaten dar. 
  
## <a name="remarks"></a>Hinweise

Der Verankerungspunkt wird zum Rubber-Banding bei aktivierter Dynamik verwendet.
  
Wenn Sie einen Verweis auf die Zelle Y Dynamics nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name* . XDynwhere-Steuerelemente.  *Name* ist der Name der Zeile mit Steuerelementen.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle X Dynamics aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionControls** <br/> |
| Zeilenindex:  <br/> |**VisRowControl** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCtlXDyn** <br/> |
   

