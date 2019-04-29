---
title: Zelle "LineJumpStyle" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251646
localization_priority: Normal
ms.assetid: 89f16674-ee1f-f5f9-9830-7bcc52e3a068
description: Bestimmt das Liniensprungformat für sämtliche Verbinder auf dem Zeichenblatt, die kein lokales Liniensprungformat haben.
ms.openlocfilehash: 066c96f659061290b825684a479432e6d71f518c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427241"
---
# <a name="linejumpstyle-cell-page-layout-section"></a>Zelle "LineJumpStyle" (Abschnitt "Page Layout")

Bestimmt das Liniensprungformat für sämtliche Verbinder auf dem Zeichenblatt, die kein lokales Liniensprungformat haben.
  
|**Wert**|**Liniensprungformat**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Bogens  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |Bogens  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Lücke  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Square  <br/> |**visLOJumpStyleSquare** <br/> |
|4  <br/> |2 Seiten  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |3 Seiten  <br/> |**visLOJumpStyle2Point** <br/> |
|6  <br/> |4 Seiten  <br/> |**visLOJumpStyle3Point** <br/> |
|7  <br/> |5 Seiten  <br/> |**visLOJumpStyle4Point** <br/> |
|8  <br/> |6 Seiten  <br/> |**visLOJumpStyle5Point** <br/> |
|9  <br/> |7 Seiten  <br/> |**visLOJumpStyle6Point** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).
  
Wenn Sie einen Verweis auf die Zelle Zelle LineJumpStyle aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle LineJumpStyle  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle LineJumpStyle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOJumpStyle** <br/> |
   

