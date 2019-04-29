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
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle für eine bestimmte Form auch im Dialogfeld **Verhalten** auf der Registerkarte **Platzierung** festlegen (bei aktiviertem Shape klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten**, und klicken Sie dann auf die Registerkarte **Platzierung** ). 
  
Wenn Sie dieses Verhalten für *alle* Formen auf dem Zeichenblatt festlegen möchten, verwenden Sie die Zelle Zelle PlowCode im Abschnitt Seiten Layout. 
  
Wenn Sie einen Verweis auf die Zelle Zelle ShapePlowCode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle ShapePlowCode  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ShapePlowCode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOPlowCode** <br/> |
   

