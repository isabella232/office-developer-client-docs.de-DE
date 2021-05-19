---
title: Zelle "LocPinY" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
localization_priority: Normal
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: 'Stellt die y-Koordinate des Drehpunkts der Form (Drehungsmitte) im Verhältnis zum Ursprung der Form dar. Die Standardformel zum Bestimmen von LocPinY ist:'
ms.openlocfilehash: e65bfec8fdcf2be1ee92c23b7afcb183c95ea9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410595"
---
# <a name="locpiny-cell-shape-transform-section"></a>Zelle "LocPinY" (Abschnitt "Shape Transform")

Stellt  die y-Koordinate des Drehpunkts der Form (Drehungsmitte) im Verhältnis zum Ursprung der Form dar. Die Standardformel zum Bestimmen von LocPinY ist: 
  
= Höhe \* 0,5
  
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die LocPinY-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LocPinY  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LocPinY-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
| Zellenindex:  <br/> |**visXFormLocPinY** <br/> |
   

