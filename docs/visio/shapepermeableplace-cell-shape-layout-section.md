---
title: Zelle "ShapePermeablePlace" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm885
localization_priority: Normal
ms.assetid: b647cbb5-2769-068d-bbda-2dc983c47ac9
description: Legt fest, ob platzierbare Shapes über einem Shape platziert werden können, wenn Shapes unter Verwendung des Dialogfelds Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu anordnen, und klicken Sie anschließend auf Weitere Layoutoptionen) ausgerichtet werden.
ms.openlocfilehash: ceecfa25c66c3ba261865d0131a3f55ef444d5e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427220"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a>Zelle "ShapePermeablePlace" (Abschnitt "Shape Layout")

Legt fest, ob platzierbare Shapes über einem Shape platziert werden können, wenn Shapes unter Verwendung des Dialogfelds **Layout konfigurieren** (klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu anordnen**, und klicken Sie anschließend auf **Weitere Layoutoptionen**) ausgerichtet werden.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Shapes können über einem Shape platziert werden.  <br/> |
|FALSE  <br/> |Shapes können nicht über einem Shape platziert werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch im Dialogfeld **Verhalten** auf der Registerkarte **Platzierung** festlegen (wenn ein Shape ausgewählt ist, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten**, und klicken Sie dann auf die Registerkarte **Platzierung** ). 
  
In Versionen vor Microsoft Visio 2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt.
  
Wenn Sie einen Verweis auf die Zelle Zelle ShapePermeablePlace aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle ShapePermeablePlace  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ShapePermeablePlace aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOPermeablePlace** <br/> |
   

