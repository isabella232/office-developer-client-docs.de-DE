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
ms.openlocfilehash: 6ae83fa70cc545c88080ce27046bd8c226c060e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798009"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a>Zelle "ShapeFixedCode" (Abschnitt "Shape Layout")

Definiert das Platzierungsverhalten für ein platzierbares Shape.
  
|**Wert**|**Auswahlmodus**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|&amp;H1  <br/> |Verschieben Sie dieses Shape nicht, wenn Shapes mithilfe des Dialogfelds **Layout konfigurieren** angeordnet werden.  <br/> |**visSLOFixedPlacement** <br/> |
|&amp;H2  <br/> |Dieses Shape nicht verschieben und nicht zulassen, dass verschiebbare Shapes darüber platziert werden.  <br/> |**visSLOFixedPlow** <br/> |
|&amp;H4  <br/> |Dieses Shape nicht verschieben, aber zulassen, dass verschiebbare Shapes darüber platziert werden.  <br/> |**visSLOFixedPermeablePlow** <br/> |
|&amp;H20 (32)  <br/> |Bei Weiterleitungen Verbindungspunktpositionen ignorieren.  <br/> |**visSLOFixedConnPtsIgnore** <br/> |
|&amp;H40 (64)  <br/> |Nur die Weiterleitung zu Seiten mit Verbindungspunkten zulassen.  <br/> |**visSLOFixedConnPtsOnly** <br/> |
|&amp;H80 (128)  <br/> |Keine Objekte an den Rand dieses Shapes kleben. Objekte stattdessen an das Ausrichtungsfeld des Shapes kleben.  <br/> |**visSLOFixedNoFoldToShape** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können den Wert dieser Zelle auch festlegen, auf der Registerkarte **Platzierung** im Dialogfeld **Verhalten** (mit einem Shape ausgewählt haben, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** klicken Sie auf **das Verhalten**, und klicken Sie dann auf die Registerkarte **Platzierung** ). 
  
Sie können eine beliebige Kombination der folgenden Werte für diese Zelle festlegen. Sie können beispielsweise den Wert 3 eingeben (&amp;H3), der das Verschieben verhindert, wenn Sie Shapes mithilfe des Dialogfelds **Layout konfigurieren** (auf der Registerkarte **Entwurf** in der Gruppe **Layout** , klicken Sie auf **Der Seite Re-Layout**, und klicken Sie dann auf ** Weitere Layoutoptionen** ) und wenn andere platzierbare Shapes auf oder in der Nähe der Shapes platziert werden. 
  
In Versionen vor Visio  2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt. 
  
Zum Abrufen eines Verweises auf die Zelle ShapeFixedCode nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapeFixedCode  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ShapeFixedCode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOFixedCode** <br/> |
   

