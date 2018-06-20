---
title: Zelle "TxtLocPinX" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: 'Legt die X--Koordinate des Textblocks des Drehung im Verhältnis zum Ursprung des Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: 6eb48532bb19bce5b0d22ed2cd0997014721df88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798313"
---
# <a name="txtlocpinx-cell-text-transform-section"></a>Zelle "TxtLocPinX" (Abschnitt "Text Transform")

Legt die *X* --Koordinate des Textblocks des Drehung im Verhältnis zum Ursprung des Textblocks. Die Standardformel lautet: 
  
= TxtWidth \* 0,5
  
Diese Formel berechnet die horizontale Mitte des Textblocks.
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle TxtLocPinX nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TxtLocPinX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle TxtLocPinX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowTextXForm** <br/> |
| Zellenindex:  <br/> |**visXFormLocPinX** <br/> |
   

