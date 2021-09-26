---
title: Zelle "ShapeFixedCode" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm880
ms.localizationpriority: medium
ms.assetid: a1736a5c-421c-2bdb-b164-76a8cd06cc3d
description: Definiert das Platzierungsverhalten für ein platzierbares Shape.
ms.openlocfilehash: 71dcee0cd60f702c138389c437c6dc4eb4895eb2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627478"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a>Zelle "ShapeFixedCode" (Abschnitt "Shape Layout")

Definiert das Platzierungsverhalten für ein platzierbares Shape.
  
|**Wert**|**Auswahlmodus**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|&amp;H1  <br/> |Verschieben Sie dieses Shape nicht, wenn Shapes mithilfe des Dialogfelds **Layout** konfigurieren angeordnet werden.  <br/> |**visSLOFixedPlacement** <br/> |
|&amp;H2  <br/> |Dieses Shape nicht verschieben und nicht zulassen, dass verschiebbare Shapes darüber platziert werden.  <br/> |**visSLOFixedPlow** <br/> |
|&amp;H4  <br/> |Dieses Shape nicht verschieben, aber zulassen, dass verschiebbare Shapes darüber platziert werden.  <br/> |**visSLOFixedPermeablePlow** <br/> |
|&amp;H20 (32)  <br/> |Bei Weiterleitungen Verbindungspunktpositionen ignorieren.  <br/> |**visSLOFixedConnPtsIgnore** <br/> |
|&amp;H40 (64)  <br/> |Nur die Weiterleitung zu Seiten mit Verbindungspunkten zulassen.  <br/> |**visSLOFixedConnPtsOnly** <br/> |
|&amp;H80 (128)  <br/> |Keine Objekte an den Rand dieses Shapes kleben. Objekte stattdessen an das Ausrichtungsfeld des Shapes kleben.  <br/> |**visSLOFixedNoFoldToShape** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch auf der Registerkarte **Platzierung** im Dialogfeld **Verhalten** festlegen (bei ausgewähltem Shape auf der Registerkarte Entwicklertools in der Gruppe Shape-Design klicken Sie auf Verhalten und anschließend auf die Registerkarte **Platzierung).** [](run-in-developer-mode-display-the-developer-tab.md)   
  
Sie können für diese Zelle jede beliebige Kombination dieser Werte festlegen. Sie können z. B. den Wert 3 ( H3) eingeben, wodurch Bewegungen beim Anordnen von Shapes mithilfe des Dialogfelds Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu anordnen &amp; und dann auf  **Weitere** Layoutoptionen und wenn  andere platzierbare Shapes auf oder in der Nähe des Shapes platziert werden) entfernt werden.   
  
In Versionen vor Microsoft Visio 2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt. 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "ShapeFixedCode" anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapeFixedCode  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapeFixedCode anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOFixedCode** <br/> |
   

