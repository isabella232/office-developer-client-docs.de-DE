---
title: Zelle "PlowCode" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251660
ms.localizationpriority: medium
ms.assetid: e43f3d29-7def-d36e-ac64-62f0a389d415
description: Legt fest, ob platzierbare Shapes verschoben werden, wenn Sie ein platzierbares Shape in der Nähe eines anderen auf dem Zeichenblatt ablegen.
ms.openlocfilehash: de96a824176c4407527ef96b18a0f1695305070c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608081"
---
# <a name="plowcode-cell-page-layout-section"></a>Zelle "PlowCode" (Abschnitt "Page Layout")

Legt fest, ob platzierbare Shapes verschoben werden, wenn Sie ein platzierbares Shape in der Nähe eines anderen auf dem Zeichenblatt ablegen.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Shapes nicht verschieben  <br/> |**visPLOPlowNone** <br/> |
|1  <br/> |Shapes verschieben  <br/> |**visPLOPlowAll** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können den Wert dieser Zelle auch auf der Registerkarte **Layout und** Routing im Dialogfeld Seite einrichten festlegen (klicken Sie auf der Registerkarte Entwurf auf den Pfeil neben Seite **einrichten),** indem Sie das Kontrollkästchen **"Andere Shapes beim Ablegen wegverschieben"** verwenden.   
  
Um einen Verweis auf die Zelle "PlowCode" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PlowCode  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PlowCode anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOPlowCode** <br/> |
   

