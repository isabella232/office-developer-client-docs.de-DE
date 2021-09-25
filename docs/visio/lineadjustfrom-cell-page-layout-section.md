---
title: Zelle "LineAdjustFrom" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251887
ms.localizationpriority: medium
ms.assetid: 6949c717-dc69-1d17-5215-eb6efce56fcb
description: Bestimmt, welche dynamischen Verbinder von der Anwendung getrennt werden, wenn diese übereinander liegen.
ms.openlocfilehash: 9cd973500652128d6189d1b48fad2fda198c22f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623425"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a>Zelle "LineAdjustFrom" (Abschnitt "Page Layout")

Bestimmt, welche dynamischen Verbinder von der Anwendung getrennt werden, wenn diese übereinander liegen.
  
|**Wert**|**Anpassung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Nicht verwandte Linien  <br/> |**visPLOLineAdjustFromNotRelated** <br/> |
|1  <br/> |Alle Linien  <br/> |**visPLOLineAdjustFromAll** <br/> |
|2  <br/> |Keine Linien  <br/> |**visPLOLineAdjustFromNone** <br/> |
|3  <br/> |Standard-Umleitungsformatvorlage  <br/> |**visPLOLineAdjustFromRoutingDefault** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).
  
Um einen Verweis auf die Zelle "LineAdjustFrom" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LineAdjustFrom  <br/> |
   
Um einen Verweis auf die Zelle "LineAdjustFrom" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOLineAdjustFrom** <br/> |
   

