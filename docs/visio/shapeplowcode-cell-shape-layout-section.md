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
ms.openlocfilehash: 5917abad653e7aaf40da05eafa3f9f1a90a2cf9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798038"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a>ShapePlowCode Cell (Shape Layout Section)

Legt fest, ob dieses platzierbare Shape verschoben wird, wenn Sie ein anderes platzierbares Shape in der Nähe dieses Shapes auf dem Zeichenblatt ablegen.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Verschieben nach Blattvorgabe.  <br/> |**visSLOPlowDefault** <br/> |
|1  <br/> |Keine Shapes verschieben.  <br/> |**visSLOPlowNever** <br/> |
|2  <br/> |Jedes Shape verschieben.  <br/> |**visSLOPlowAlways** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können auch den Wert dieser Zelle für ein bestimmtes Shape auf der Registerkarte **Platzierung** im Dialogfeld **Verhalten** festlegen (klicken Sie mit einem Shape ausgewählt haben, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten**, und klicken Sie dann auf die Registerkarte **Platzierung** ). 
  
Wenn Sie dieses Verhalten für *sämtliche* Shapes auf dem Zeichenblatt festlegen möchten, verwenden Sie die Zelle PlowCode im Abschnitt Page Layout. 
  
Wenn Sie einen Verweis auf die Zelle ShapePlowCode nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapePlowCode  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ShapePlowCode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOPlowCode** <br/> |
   

