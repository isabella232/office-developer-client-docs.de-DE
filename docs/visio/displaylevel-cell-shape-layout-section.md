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
ms.openlocfilehash: 516446b2d401aaca614e24a2c5bb5003fafe8574
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796836"
---
# <a name="displaylevel-cell-shape-layout-section"></a>DisplayLevel Cell (Shape Layout Section)

Bestimmt den Anzeigeebenenbereich (den relativen Bereich der Gruppierung in Z-Reihenfolge) für das Shape.
  
## <a name="remarks"></a>Bemerkungen

Die Z-Reihenfolge ist die Anzeigereihenfolge für Shapes auf dem Zeichenblatt. Ein Shape, das sich in der Z-Reihenfolge weiter oben befindet, wird vor einem Shape anzeigt, das sich in der Z-Reihenfolge weiter unten befindet, wenn eines der Shapes das andere überlagert. 
  
Mit der Anzeigeebene werden Shapes in Gruppierungen oder Bereiche aufgeteilt. Alle Shapes in einem gegebenen Bereich haben eine höhere Z-Reihenfolge als die Shapes in einem niedrigeren Bereich. Standardmäßig weisen die meisten Shapes eine Anzeigeebene von 0 (null) auf.
  
Der Bereich der Anzeigeebenen rangiert von -32.767 bis +32.767. Shapes mit der gleichen Anzeigeebene werden zu einem einzigen Bereich zusammengefasst, in dem sie ebenfalls gemäß der Z-Reihenfolge relativ zueinander in eine Rangfolge gesetzt werden.
  
Sie können mithilfe der Befehle **In den Vordergrund**, **Eine Ebene nach hinten**, **in den Vordergrund**und **in den Hintergrund**der Z-Ordnung der Formen einen Streifen ändern. Diese Befehle eine Form aus der angegebenen Band verschieben, zeigt Microsoft Visio den reservierten Wert-32768 in Zelle DisplayLevel des Shapes, sofern die Zelle geschützt ist. In diesem Fall die Form nicht in einem anderen Band verschoben werden, und Visio zeigt die Warnung "Schutz und/oder Layer Formeigenschaften verhindern Ausführung dieses Befehls abgeschlossen". 
  
Zum Abrufen eines Verweises auf die Zelle DisplayLevel nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes. 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |DisplayLevel  <br/> |
   
Wenn Sie einen Verweis auf die Zelle DisplayLevel aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLODisplayLevel** <br/> |
   

