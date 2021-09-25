---
title: Zelle "LineJumpStyle" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251646
ms.localizationpriority: medium
ms.assetid: 89f16674-ee1f-f5f9-9830-7bcc52e3a068
description: Bestimmt das Liniensprungformat für sämtliche Verbinder auf dem Zeichenblatt, die kein lokales Liniensprungformat haben.
ms.openlocfilehash: 78f1003c5f1afac945edd31bf82fb64732b8da1e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603669"
---
# <a name="linejumpstyle-cell-page-layout-section"></a>Zelle "LineJumpStyle" (Abschnitt "Page Layout")

Bestimmt das Liniensprungformat für sämtliche Verbinder auf dem Zeichenblatt, die kein lokales Liniensprungformat haben.
  
|**Wert**|**Liniensprungformat**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Arc  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |Arc  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Lücke  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Square  <br/> |**visLOJumpStyleSquare** <br/> |
|4   <br/> |2 Seiten  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |3 Seiten  <br/> |**visLOJumpStyle2Point** <br/> |
|6   <br/> |4 Seiten  <br/> |**visLOJumpStyle3Point** <br/> |
|7   <br/> |5 Seiten  <br/> |**visLOJumpStyle4Point** <br/> |
|8   <br/> |6 Seiten  <br/> |**visLOJumpStyle5Point** <br/> |
|9   <br/> |7 Seiten  <br/> |**visLOJumpStyle6Point** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).
  
Um einen Verweis auf die Zelle "LineJumpStyle" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LineJumpStyle  <br/> |
   
Um einen Verweis auf die Zelle "LineJumpStyle" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOJumpStyle** <br/> |
   

