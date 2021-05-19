---
title: Zelle "ShapePlowCode" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
localization_priority: Normal
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: Legt fest, ob dieses platzierbare Shape verschoben wird, wenn Sie ein anderes platzierbares Shape in der Nähe dieses Shapes auf dem Zeichenblatt ablegen.
ms.openlocfilehash: 6e155103f7bfc70a78826297f441fc9ce78942ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423895"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a>Zelle "ShapePlowCode" (Abschnitt "Shape Layout")

Legt fest, ob dieses platzierbare Shape verschoben wird, wenn Sie ein anderes platzierbares Shape in der Nähe dieses Shapes auf dem Zeichenblatt ablegen.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Verschieben nach Blattvorgabe.  <br/> |**visSLOPlowDefault** <br/> |
|1  <br/> |Keine Shapes verschieben.  <br/> |**visSLOPlowNever** <br/> |
|2  <br/> |Jedes Shape verschieben.  <br/> |**visSLOPlowAlways** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können den Wert dieser Zelle für eine bestimmte Form auch auf der Registerkarte Platzierung [](run-in-developer-mode-display-the-developer-tab.md) im Dialogfeld Verhalten festlegen (wenn eine Form ausgewählt  ist, klicken Sie auf der Registerkarte Entwickler in der Gruppe **Shape-Entwurf** auf  **Verhalten,** und klicken Sie dann auf die Registerkarte Platzierung).  
  
Verwenden Sie zum Festlegen dieses Verhaltens für  *alle*  Formen auf dem Zeichenblatt die Zelle PlowCode im Abschnitt Seitenlayout. 
  
Um einen Verweis auf die Zelle ShapePlowCode anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapePlowCode  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapePlowCode nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOPlowCode** <br/> |
   

