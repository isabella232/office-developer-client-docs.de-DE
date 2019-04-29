---
title: Zelle "ConLineJumpStyle" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251655
localization_priority: Normal
ms.assetid: baa05a50-97d0-3769-635e-0ea20317d59a
description: Bestimmt das Liniensprungformat für Liniensprünge bei einem dynamischen Verbinder.
ms.openlocfilehash: ae8af4e326a6c895b3617a4869f98eaf0db68db1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415992"
---
# <a name="conlinejumpstyle-cell-shape-layout-section"></a>Zelle "ConLineJumpStyle" (Abschnitt "Shape Layout")

Bestimmt das Liniensprungformat für Liniensprünge bei einem dynamischen Verbinder.
  
|**Wert**|**Liniensprungformat**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Zeichenblattstandard  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |Bogens  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Lücke  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Square  <br/> |**visLOJumpStyleSquare** <br/> |
|4  <br/> |Dreieck  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |3 Seiten  <br/> |**visLOJumpStyle2Point** <br/> |
|6  <br/> |4 Seiten  <br/> |**visLOJumpStyle3Point** <br/> |
|7  <br/> |5 Seiten  <br/> |**visLOJumpStyle4Point** <br/> |
|8  <br/> |6 Seiten  <br/> |**visLOJumpStyle5Point** <br/> |
|9  <br/> |7 Seiten  <br/> |**visLOJumpStyle6Point** <br/> |
   
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOJumpStyle** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch festlegen, indem Sie einen dynamischen Verbinder auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten** klicken und dann auf die Registerkarte **Verbinder** klicken. 
  
Wenn Sie einen Verweis auf die Zelle Zelle ConLineJumpStyle aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle ConLineJumpStyle  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ConLineJumpStyle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  

