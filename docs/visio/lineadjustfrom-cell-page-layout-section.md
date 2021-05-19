---
title: Zelle "LineAdjustFrom" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251887
localization_priority: Normal
ms.assetid: 6949c717-dc69-1d17-5215-eb6efce56fcb
description: Bestimmt, welche dynamischen Verbinder von der Anwendung getrennt werden, wenn diese übereinander liegen.
ms.openlocfilehash: 3eb9f5513ee3ce2f5dce96cb47c356bca29a289c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415187"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a>Zelle "LineAdjustFrom" (Abschnitt "Page Layout")

Bestimmt, welche dynamischen Verbinder von der Anwendung getrennt werden, wenn diese übereinander liegen.
  
|**Wert**|**Anpassung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Nicht verwandte Linien  <br/> |**visPLOLineAdjustFromNotRelated** <br/> |
|1  <br/> |Alle Linien  <br/> |**visPLOLineAdjustFromAll** <br/> |
|2  <br/> |Keine Linien  <br/> |**visPLOLineAdjustFromNone** <br/> |
|3  <br/> |Standard-Umleitungsformatvorlage  <br/> |**visPLOLineAdjustFromRoutingDefault** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).
  
Um einen Verweis auf die Zelle LineAdjustFrom anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LineAdjustFrom  <br/> |
   
Um einen Verweis auf die LineAdjustFrom-Zelle nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOLineAdjustFrom** <br/> |
   

