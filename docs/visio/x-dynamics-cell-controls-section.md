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
description: Stellt die x-Koordinate für den Verankerungspunkt eines Steuerelements in lokalen Koordinaten dar.
ms.openlocfilehash: 7aef1fe779ae9b862e88eccf0112eb8696377858
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322302"
---
# <a name="x-dynamics-cell-controls-section"></a>Zelle "X Dynamics" (Abschnitt "Controls")

Stellt die *x* -Koordinate für den Verankerungspunkt eines Steuerelements in lokalen Koordinaten dar. 
  
## <a name="remarks"></a>Bemerkungen

Der Verankerungspunkt wird zum Rubber-Banding bei aktivierter Dynamik verwendet.
  
Wenn Sie einen Verweis auf die Zelle X Dynamics aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name* . XDynwhere-Steuerelemente.  *Name* ist der Name der Zeile Controls.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle X Dynamics nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionControls** <br/> |
| Zeilenindex:  <br/> |**visRowControl** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCtlXDyn** <br/> |
   

