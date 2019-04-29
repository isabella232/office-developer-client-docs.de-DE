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
description: 'Stellt die y-Koordinate der PIN des Shapes (Drehmittelpunkt) im Verhältnis zum Ursprung der Form dar. Die Standardformel für die Bestimmung von Zelle LocPinY lautet:'
ms.openlocfilehash: e65bfec8fdcf2be1ee92c23b7afcb183c95ea9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410595"
---
# <a name="locpiny-cell-shape-transform-section"></a>Zelle "LocPinY" (Abschnitt "Shape Transform")

Stellt die *y* -Koordinate der PIN des Shapes (Drehmittelpunkt) im Verhältnis zum Ursprung der Form dar. Die Standardformel für die Bestimmung von Zelle LocPinY lautet: 
  
= Höhe \* 0,5
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle LocPinY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle LocPinY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle LocPinY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
| Zellenindex:  <br/> |**visXFormLocPinY** <br/> |
   

