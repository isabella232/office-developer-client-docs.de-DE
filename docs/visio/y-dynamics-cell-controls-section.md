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
description: Represents the y -coordinate for a control handle's anchor point in local coordinates. Der Verankerungspunkt wird zum Rubber-Banding bei aktivierter Dynamik verwendet.
ms.openlocfilehash: 13d463ebccd9cc7a23641a036dc5dd967513b07f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404827"
---
# <a name="y-dynamics-cell-controls-section"></a>Zelle "Y Dynamics" (Abschnitt "Controls")

Represents the  *y*  -coordinate for a control handle's anchor point in local coordinates. Der Verankerungspunkt wird zum "Rubber-Banding" bei aktivierter Dynamik verwendet. 
  
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle Y Dynamics anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name*  . YDynwhere-Steuerelemente.  *name*  ist der Name der Steuerelementzeile.  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Y Dynamics nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionControls** <br/> |
| Zeilenindex:  <br/> |**visRowControl**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCtlYDyn** <br/> |
   

