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
description: 'Stellt die y--Koordinate der Drehbezugspunkts (Drehmittelpunkts) im Verhältnis zum Ursprung des Shapes. Die Standardformel zum Bestimmen von LocPinY lautet:'
ms.openlocfilehash: 8d98906e8082af0fc54bc01fe3a8537b66ac56b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797412"
---
# <a name="locpiny-cell-shape-transform-section"></a>LocPinY Cell (Shape Transform Section)

Stellt die *y* --Koordinate der Drehbezugspunkts (Drehmittelpunkts) im Verhältnis zum Ursprung des Shapes. Die Standardformel zum Bestimmen von LocPinY lautet: 
  
= Höhe \* 0,5
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle LocPinY aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LocPinY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle LocPinY aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
| Zellenindex:  <br/> |**visXFormLocPinY** <br/> |
   

