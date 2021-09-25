---
title: Zelle "DisplayLevel" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80001
ms.localizationpriority: medium
ms.assetid: 08b730c4-5dd8-106e-ddf3-da2c942e2ef6
description: Bestimmt den Anzeigeebenenbereich (den relativen Bereich der Gruppierung in Z-Reihenfolge) für das Shape.
ms.openlocfilehash: bd40078d29147a40be940d40f5f059d20a3d9979
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628458"
---
# <a name="displaylevel-cell-shape-layout-section"></a>Zelle "DisplayLevel" (Abschnitt "Shape Layout")

Bestimmt den Anzeigeebenenbereich (den relativen Bereich der Gruppierung in Z-Reihenfolge) für das Shape.
  
## <a name="remarks"></a>Bemerkungen

Die Z-Reihenfolge ist die Anzeigereihenfolge für Shapes auf dem Zeichenblatt. Ein Shape, das sich in der Z-Reihenfolge weiter oben befindet, wird vor einem Shape anzeigt, das sich in der Z-Reihenfolge weiter unten befindet, wenn eines der Shapes das andere überlagert. 
  
Mit der Anzeigeebene werden Shapes in Gruppierungen oder Bereiche aufgeteilt. Alle Shapes in einem gegebenen Bereich haben eine höhere Z-Reihenfolge als die Shapes in einem niedrigeren Bereich. Standardmäßig weisen die meisten Shapes eine Anzeigeebene von 0 (null) auf.
  
Der Bereich der Anzeigeebenen rangiert von -32.767 bis +32.767. Shapes mit der gleichen Anzeigeebene werden zu einem einzigen Bereich zusammengefasst, in dem sie ebenfalls gemäß der Z-Reihenfolge relativ zueinander in eine Rangfolge gesetzt werden.
  
Sie können die Z-Reihenfolge von Formen innerhalb eines Bandes ändern, indem Sie die Befehle **"Vorwärts",** **"Zurück senden",** **"Nach vorne"** und **"Zurück"** verwenden. Wird ein Shape mit diesen Befehlen aus dem angestammten Bereich verschoben, zeigt Microsoft Visio den reservierten Wert -32768 in der Zelle "DisplayLevel" des Shapes an, sofern die Zelle nicht geschützt ist. In dem Fall kann das Shape nicht in einen anderen Bereich verschoben werden, und Visio gibt die Warnung "Aktiver Shape-Schutz oder Container- und/oder Layereigenschaften verhindern die vollständige Ausführung dieses Befehls" aus. 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle DisplayLevel anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen. 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |DisplayLevel  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle DisplayLevel anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLODisplayLevel** <br/> |
   

