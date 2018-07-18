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
ms.openlocfilehash: 96941f675b67b38a8575bd712db5ad0eb76cd50f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797334"
---
# <a name="linejumpstyle-cell-page-layout-section"></a>LineJumpStyle Cell (Page Layout Section)

Bestimmt das Liniensprungformat für sämtliche Verbinder auf dem Zeichenblatt, die kein lokales Liniensprungformat haben.
  
|**Wert**|**Liniensprungformat**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Bogen  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |Bogen  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Lücke  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Quadrat  <br/> |**visLOJumpStyleSquare** <br/> |
|4  <br/> |2 Seiten  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |3 Seiten  <br/> |**visLOJumpStyle2Point** <br/> |
|6  <br/> |4 Seiten  <br/> |**visLOJumpStyle3Point** <br/> |
|7  <br/> |5 Seiten  <br/> |**visLOJumpStyle4Point** <br/> |
|8  <br/> |6 Seiten  <br/> |**visLOJumpStyle5Point** <br/> |
|9  <br/> |7 Seiten  <br/> |**visLOJumpStyle6Point** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).
  
Wenn Sie einen Verweis auf die Zelle LineJumpStyle aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LineJumpStyle  <br/> |
   
Wenn Sie einen Verweis auf die Zelle LineJumpStyle aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOJumpStyle** <br/> |
   

