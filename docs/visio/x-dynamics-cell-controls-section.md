---
title: Zelle "X Dynamics" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
ms.localizationpriority: medium
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: Stellt die X-Koordinate für den Ankerpunkt eines Steuerpunkts in lokalen Koordinaten dar.
ms.openlocfilehash: 9389d8e0974a5f89bfc4eee18b107dab5b0c25ca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559332"
---
# <a name="x-dynamics-cell-controls-section"></a>Zelle "X Dynamics" (Abschnitt "Controls")

Stellt  die X-Koordinate für den Ankerpunkt eines Steuerpunkts in lokalen Koordinaten dar. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Der Verankerungspunkt wird zum Rubber-Banding bei aktivierter Dynamik verwendet.
  
Um einen Verweis auf die Zelle X Dynamics anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name*  . XDynwhere-Steuerelemente.  *Name*  ist der Name der Steuerelementzeile.  <br/> |
   
Um einen Verweis auf die Zelle X Dynamics anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionControls** <br/> |
| Zeilenindex:  <br/> |**visRowControl**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCtlXDyn** <br/> |
   

