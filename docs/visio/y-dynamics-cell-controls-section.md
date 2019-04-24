---
title: Zelle "Y Dynamics" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
localization_priority: Normal
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: Stellt die y-Koordinate für den Verankerungspunkt eines Steuerelements in lokalen Koordinaten dar. Der Verankerungspunkt wird zum Rubber-Banding bei aktivierter Dynamik verwendet.
ms.openlocfilehash: 13d463ebccd9cc7a23641a036dc5dd967513b07f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341181"
---
# <a name="y-dynamics-cell-controls-section"></a>Zelle "Y Dynamics" (Abschnitt "Controls")

Stellt die *y* -Koordinate für den Verankerungspunkt eines Steuerelements in lokalen Koordinaten dar. Der Verankerungspunkt wird zum "Rubber-Banding" bei aktivierter Dynamik verwendet. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Y Dynamics aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name* . YDynwhere-Steuerelemente.  *Name* ist der Name der Zeile Controls.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Y Dynamics nach Index aus einem Programm abrufen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionControls** <br/> |
| Zeilenindex:  <br/> |**visRowControl** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCtlYDyn** <br/> |
   

