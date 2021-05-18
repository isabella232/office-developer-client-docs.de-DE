---
title: Zelle "LineAdjustTo" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
localization_priority: Normal
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: Legt fest, welche dynamischen Verbinder übereinander liegen.
ms.openlocfilehash: e4fb32c0fcb488173324ea597edc2c9d13f6bfca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414025"
---
# <a name="lineadjustto-cell-page-layout-section"></a>Zelle "LineAdjustTo" (Abschnitt "Page Layout")

Legt fest, welche dynamischen Verbinder übereinander liegen.
  
|**Wert**|**Anpassung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Standard-Umleitungsformatvorlage  <br/> |**visPLOLineAdjustToDefault** <br/> |
|1  <br/> |Linien, die nahe beieinander liegen.  <br/> |**visPLOLineAdjustToAll** <br/> |
|2  <br/> |Keine Linien  <br/> |**visPLOLineAdjustToNone** <br/> |
|3  <br/> |Verwandte Linien  <br/> |**visPLOLineAdjustToRelated** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).
  
Um einen Verweis auf die Zelle LineAdjustTo anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LineAdjustTo  <br/> |
   
Um einen Verweis auf die LineAdjustTo-Zelle nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOLineAdjustTo** <br/> |
   

