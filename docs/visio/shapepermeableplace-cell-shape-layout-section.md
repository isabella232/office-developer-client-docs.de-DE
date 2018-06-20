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
description: Bestimmt, ob platzierbare Shapes über einem Shape platziert werden können, wenn Shapes im Dialogfeld Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout, klicken Sie auf der Seite Re-Layout, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 1873575eb4322d31f81c0dd34557c6167750ce82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798018"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a>Zelle "ShapePermeablePlace" (Abschnitt "Shape Layout")

Bestimmt, ob platzierbare Shapes über einem Shape platziert werden können, wenn Shapes im Dialogfeld **Layout konfigurieren** (auf der Registerkarte **Entwurf** in der Gruppe **Layout** klicken Sie auf **Der Seite Re-Layout**, und klicken Sie dann auf **Weitere Layout-Optionen **).
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Shapes können über einem Shape platziert werden.  <br/> |
|FALSE  <br/> |Shapes können nicht über einem Shape platziert werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch festlegen, auf der Registerkarte **Platzierung** im Dialogfeld **Verhalten** (mit einem Shape ausgewählt haben, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** klicken Sie auf **das Verhalten**, und klicken Sie dann auf die Registerkarte **Platzierung** ). 
  
In Versionen vor Visio  2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt.
  
Zum Abrufen eines Verweises auf die Zelle ShapePermeablePlace nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapePermeablePlace  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ShapePermeablePlace aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOPermeablePlace** <br/> |
   

