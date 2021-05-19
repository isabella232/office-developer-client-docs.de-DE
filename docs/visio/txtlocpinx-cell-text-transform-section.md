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
description: 'Bestimmt die x-Koordinate des Drehzentrums des Textblocks im Verhältnis zum Ursprung des Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: 390f8129e8000a043969eda0ab1c8e4ef62515ef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425855"
---
# <a name="txtlocpinx-cell-text-transform-section"></a>Zelle "TxtLocPinX" (Abschnitt "Text Transform")

Bestimmt  die x-Koordinate des Drehzentrums des Textblocks im Verhältnis zum Ursprung des Textblocks. Die Standardformel lautet: 
  
= TxtWidth \* 0,5
  
Diese Formel berechnet die horizontale Mitte des Textblocks.
  
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle TxtLocPinX anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TxtLocPinX  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle TxtLocPinX nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowTextXForm** <br/> |
| Zellenindex:  <br/> |**visXFormLocPinX** <br/> |
   

