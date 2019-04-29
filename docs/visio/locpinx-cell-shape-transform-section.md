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
description: 'Stellt die x-Koordinate der PIN des Shapes (Drehmittelpunkt) im Verhältnis zum Ursprung der Form dar. Die Standardformel für die Bestimmung von Zelle LocPinX lautet:'
ms.openlocfilehash: 2eb5c328eed3c97652173670c426b83b8c358833
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439240"
---
# <a name="locpinx-cell-shape-transform-section"></a>Zelle "LocPinX" (Abschnitt "Shape Transform")

Stellt die *x* -Koordinate der PIN des Shapes (Drehmittelpunkt) im Verhältnis zum Ursprung der Form dar. Die Standardformel für die Bestimmung von Zelle LocPinX lautet: 
  
= Breite \* 0,5
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle LocPinX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle LocPinX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle LocPinX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
| Zellenindex:  <br/> |**visXFormLocPinX** <br/> |
   

