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
ms.openlocfilehash: 13540f9dc5e6e6861d3f3679bcf49204d553397a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797324"
---
# <a name="lineadjustto-cell-page-layout-section"></a>LineAdjustTo Cell (Page Layout Section)

Legt fest, welche dynamischen Verbinder übereinander liegen.
  
|**Wert**|**Anpassung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Standard-Umleitungsformatvorlage  <br/> |**visPLOLineAdjustToDefault** <br/> |
|1  <br/> |Linien, die nahe beieinander liegen.  <br/> |**visPLOLineAdjustToAll** <br/> |
|2  <br/> |Keine Linien  <br/> |**visPLOLineAdjustToNone** <br/> |
|3  <br/> |Verwandte Linien  <br/> |**visPLOLineAdjustToRelated** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können den Wert dieser Zelle auch festlegen, auf der Registerkarte **Layout und Routing** im Dialogfeld **Seite einrichten** (klicken Sie auf der Registerkarte **Entwurf** , klicken Sie auf den Pfeil neben **Seite einrichten** , und klicken Sie dann auf **Layout und Routing**).
  
Wenn Sie einen Verweis auf die Zelle LineAdjustTo nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LineAdjustTo  <br/> |
   
Wenn Sie einen Verweis auf die Zelle LineAdjustTo aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOLineAdjustTo** <br/> |
   

