---
title: Zelle "TxtAngle" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251272
localization_priority: Normal
ms.assetid: b8482cd8-5205-40ef-b4e1-4ceb197ac80f
description: Bestimmt den Textblock aktuellen Winkel der Drehung in Bezug auf die X-Achse der Form. Der Standardwert ist 0 Grad.
ms.openlocfilehash: 08ed4422392a355db948fa947abdfd3772dec0a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798318"
---
# <a name="txtangle-cell-text-transform-section"></a>Zelle "TxtAngle" (Abschnitt "Text Transform")

Bestimmt den Textblock aktuellen Winkel der Drehung in Bezug auf die *X* -Achse der Form. Der Standardwert ist 0 Grad. 
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle TxtAngle nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TxtAngle  <br/> |
   
Wenn Sie einen Verweis auf die Zelle TxtAngle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowTextXForm** <br/> |
| Zellenindex:  <br/> |**visXFormAngle** <br/> |
   

