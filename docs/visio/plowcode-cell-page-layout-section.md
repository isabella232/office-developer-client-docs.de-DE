---
title: Zelle "PlowCode" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251660
localization_priority: Normal
ms.assetid: e43f3d29-7def-d36e-ac64-62f0a389d415
description: Legt fest, ob platzierbare Shapes verschoben werden, wenn Sie ein platzierbares Shape in der Nähe eines anderen auf dem Zeichenblatt ablegen.
ms.openlocfilehash: 4ea85ddbaf7662305a2a82fc7f0b814019624841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420353"
---
# <a name="plowcode-cell-page-layout-section"></a>Zelle "PlowCode" (Abschnitt "Page Layout")

Legt fest, ob platzierbare Shapes verschoben werden, wenn Sie ein platzierbares Shape in der Nähe eines anderen auf dem Zeichenblatt ablegen.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Shapes nicht verschieben  <br/> |**visPLOPlowNone** <br/> |
|1  <br/> |Shapes verschieben  <br/> |**visPLOPlowAll** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können den Wert dieser Zelle auch auf der  Registerkarte **Layout** und  Routing im Dialogfeld Seiteneinrichtung festlegen (klicken Sie auf der Registerkarte Entwurf auf den Pfeil Seite **einrichten),** indem Sie das Kontrollkästchen Andere Shapes beim Ablegen weg verschieben aktivieren.  
  
Um einen Verweis auf die PlowCode-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PlowCode  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die PlowCode-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOPlowCode** <br/> |
   

