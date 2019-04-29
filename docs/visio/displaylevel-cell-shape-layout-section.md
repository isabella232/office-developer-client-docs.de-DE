---
title: Zelle "DisplayLevel" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80001
localization_priority: Normal
ms.assetid: 08b730c4-5dd8-106e-ddf3-da2c942e2ef6
description: Bestimmt den Anzeigeebenenbereich (den relativen Bereich der Gruppierung in Z-Reihenfolge) für das Shape.
ms.openlocfilehash: 4f7e3fcb2d28f8c4c0706502c66444c121ae6ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408145"
---
# <a name="displaylevel-cell-shape-layout-section"></a>Zelle "DisplayLevel" (Abschnitt "Shape Layout")

Bestimmt den Anzeigeebenenbereich (den relativen Bereich der Gruppierung in Z-Reihenfolge) für das Shape.
  
## <a name="remarks"></a>Bemerkungen

Die Z-Reihenfolge ist die Anzeigereihenfolge für Shapes auf dem Zeichenblatt. Ein Shape, das sich in der Z-Reihenfolge weiter oben befindet, wird vor einem Shape anzeigt, das sich in der Z-Reihenfolge weiter unten befindet, wenn eines der Shapes das andere überlagert. 
  
Mit der Anzeigeebene werden Shapes in Gruppierungen oder Bereiche aufgeteilt. Alle Shapes in einem gegebenen Bereich haben eine höhere Z-Reihenfolge als die Shapes in einem niedrigeren Bereich. Standardmäßig weisen die meisten Shapes eine Anzeigeebene von 0 (null) auf.
  
Der Bereich der Anzeigeebenen rangiert von -32.767 bis +32.767. Shapes mit der gleichen Anzeigeebene werden zu einem einzigen Bereich zusammengefasst, in dem sie ebenfalls gemäß der Z-Reihenfolge relativ zueinander in eine Rangfolge gesetzt werden.
  
Sie können die Z-Reihenfolge von Formen innerhalb eines Bands ändern, indem Sie die Befehle nach **vorn**, nach **hinten**, **nach vorn**und nach **hinten**senden verwenden. Wird ein Shape mit diesen Befehlen aus dem angestammten Bereich verschoben, zeigt Microsoft Visio den reservierten Wert -32768 in der Zelle "DisplayLevel" des Shapes an, sofern die Zelle nicht geschützt ist. In dem Fall kann das Shape nicht in einen anderen Bereich verschoben werden, und Visio gibt die Warnung "Aktiver Shape-Schutz oder Container- und/oder Layereigenschaften verhindern die vollständige Ausführung dieses Befehls" aus. 
  
Wenn Sie einen Verweis auf die Zelle Display Level aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes. 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Display Level  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Display Level aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLODisplayLevel** <br/> |
   

