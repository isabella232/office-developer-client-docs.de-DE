---
title: Zelle "LocPinY" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
ms.localizationpriority: medium
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: 'Stellt die y-Koordinate des Drehbezugs (Drehmittelpunkt) des Shapes im Verhältnis zum Ursprung des Shapes dar. Die Standardformel für die Ermittlung von LocPinY lautet:'
ms.openlocfilehash: 3e9ff2fd0daf3f75e1e1b341a37836e0ccc70831
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623362"
---
# <a name="locpiny-cell-shape-transform-section"></a>Zelle "LocPinY" (Abschnitt "Shape Transform")

Stellt  die y-Koordinate des Drehbezugs (Drehmittelpunkt) des Shapes im Verhältnis zum Ursprung des Shapes dar. Die Standardformel für die Ermittlung von LocPinY lautet: 
  
= Höhe \* 0,5
  
## <a name="remarks"></a>Bemerkungen

Um einen Verweis auf die Zelle "LocPinY" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LocPinY  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LocPinY anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
| Zellenindex:  <br/> |**visXFormLocPinY** <br/> |
   

