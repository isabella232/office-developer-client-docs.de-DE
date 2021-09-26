---
title: Zelle "LineAdjustTo" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
ms.localizationpriority: medium
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: Legt fest, welche dynamischen Verbinder übereinander liegen.
ms.openlocfilehash: 5f0d12107f760d9e442ab733fa8a03bb4bda6f55
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618658"
---
# <a name="lineadjustto-cell-page-layout-section"></a>Zelle "LineAdjustTo" (Abschnitt "Page Layout")

Legt fest, welche dynamischen Verbinder übereinander liegen.
  
|**Wert**|**Anpassung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Standard-Umleitungsformatvorlage  <br/> |**visPLOLineAdjustToDefault** <br/> |
|1  <br/> |Linien, die nahe beieinander liegen.  <br/> |**visPLOLineAdjustToAll** <br/> |
|2  <br/> |Keine Linien  <br/> |**visPLOLineAdjustToNone** <br/> |
|3  <br/> |Verwandte Linien  <br/> |**visPLOLineAdjustToRelated** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).
  
Um einen Verweis auf die Zelle "LineAdjustTo" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LineAdjustTo  <br/> |
   
Um einen Verweis auf die Zelle "LineAdjustTo" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOLineAdjustTo** <br/> |
   

