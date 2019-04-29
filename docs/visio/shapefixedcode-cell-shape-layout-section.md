---
title: Zelle "ShapeFixedCode" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm880
localization_priority: Normal
ms.assetid: a1736a5c-421c-2bdb-b164-76a8cd06cc3d
description: Definiert das Platzierungsverhalten für ein platzierbares Shape.
ms.openlocfilehash: eae44a0579129fbe8da1c0cc8c37318beb024563
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431743"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a>Zelle "ShapeFixedCode" (Abschnitt "Shape Layout")

Definiert das Platzierungsverhalten für ein platzierbares Shape.
  
|**Wert**|**Auswahlmodus**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|&amp;H1  <br/> |Verschieben Sie dieses Shape nicht, wenn Shapes mithilfe des Dialogfelds **Layout konfigurieren** festgelegt werden.  <br/> |**visSLOFixedPlacement** <br/> |
|&amp;H2  <br/> |Dieses Shape nicht verschieben und nicht zulassen, dass verschiebbare Shapes darüber platziert werden.  <br/> |**visSLOFixedPlow** <br/> |
|&amp;H4  <br/> |Dieses Shape nicht verschieben, aber zulassen, dass verschiebbare Shapes darüber platziert werden.  <br/> |**visSLOFixedPermeablePlow** <br/> |
|&amp;H20 (32)  <br/> |Bei Weiterleitungen Verbindungspunktpositionen ignorieren.  <br/> |**visSLOFixedConnPtsIgnore** <br/> |
|&amp;H40 (64)  <br/> |Nur die Weiterleitung zu Seiten mit Verbindungspunkten zulassen.  <br/> |**visSLOFixedConnPtsOnly** <br/> |
|&amp;H80 (128)  <br/> |Keine Objekte an den Rand dieses Shapes kleben. Objekte stattdessen an das Ausrichtungsfeld des Shapes kleben.  <br/> |**visSLOFixedNoFoldToShape** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch im Dialogfeld **Verhalten** auf der Registerkarte **Platzierung** festlegen (wenn ein Shape ausgewählt ist, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten**, und klicken Sie dann auf die Registerkarte **Platzierung** ). 
  
Sie können für diese Zelle jede beliebige Kombination dieser Werte festlegen. Sie können beispielsweise den Wert 3&amp;(H3) eingeben, der beim Layout von Shapes mithilfe des Dialogfelds **Layout konfigurieren** (Klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu Layout**), und klicken Sie dann auf ** Weitere Layoutoptionen** ) und wenn andere Platzierungs Formen auf oder in der Nähe der Form platziert werden. 
  
In Versionen vor Microsoft Visio 2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt. 
  
Wenn Sie einen Verweis auf die Zelle Zelle ShapeFixedCode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle ShapeFixedCode  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ShapeFixedCode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOFixedCode** <br/> |
   

