---
title: Zelle "LocPinX" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm680
localization_priority: Normal
ms.assetid: b82feade-5793-8a6e-3ff4-69a4cbdd2cf9
description: 'Stellt die X--Koordinate der Drehbezugspunkts (Drehmittelpunkts) im Verhältnis zum Ursprung des Shapes. Die Standardformel zum Bestimmen von LocPinX lautet:'
ms.openlocfilehash: 17f7b0fde9a54f6596f2f87f866d30b908e062b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797425"
---
# <a name="locpinx-cell-shape-transform-section"></a>Zelle "LocPinX" (Abschnitt "Shape Transform")

Stellt die *X* --Koordinate der Drehbezugspunkts (Drehmittelpunkts) im Verhältnis zum Ursprung des Shapes. Die Standardformel zum Bestimmen von LocPinX lautet: 
  
= Breite \* 0,5
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle LocPinX nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LocPinX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle LocPinX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
| Zellenindex:  <br/> |**visXFormLocPinX** <br/> |
   

