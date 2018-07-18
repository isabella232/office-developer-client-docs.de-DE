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
ms.openlocfilehash: ee3a107f7e19b53017c2ea24c94babceb49620d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797313"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a>LineAdjustFrom Cell (Page Layout Section)

Bestimmt, welche dynamischen Verbinder von der Anwendung getrennt werden, wenn diese übereinander liegen.
  
|**Wert**|**Ausrichtung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Nicht verwandte Linien  <br/> |**visPLOLineAdjustFromNotRelated** <br/> |
|1  <br/> |Alle Linien  <br/> |**visPLOLineAdjustFromAll** <br/> |
|2  <br/> |Keine Linien  <br/> |**visPLOLineAdjustFromNone** <br/> |
|3  <br/> |Standard-Umleitungsformatvorlage  <br/> |**visPLOLineAdjustFromRoutingDefault** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).
  
Wenn Sie einen Verweis auf die Zelle LineAdjustFrom aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LineAdjustFrom  <br/> |
   
Wenn Sie einen Verweis auf die Zelle LineAdjustFrom aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOLineAdjustFrom** <br/> |
   

