---
title: Zelle "ResizePage" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
localization_priority: Normal
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: Bestimmt, ob die Seite vergrößert werden soll, um die Zeichnung mit einzuschließen, nachdem Shapes mithilfe des Dialogfelds Layout konfigurieren ausgerichtet wurden (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu anordnen, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 8d0001ce35808f8c5f11068ed78865ce992af5cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438092"
---
# <a name="resizepage-cell-page-layout-section"></a>Zelle "ResizePage" (Abschnitt "Page Layout")

Bestimmt, ob die Seite vergrößert werden soll, um die Zeichnung nach dem Layout von Shapes zu schließen, indem Sie das Dialogfeld **Layout** konfigurieren verwenden (klicken Sie auf der Registerkarte **Entwurf** in der **Gruppe Layout** auf **Seite** neu layout, und klicken Sie dann auf Weitere **Layoutoptionen**).
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Blatt vergrößern.  <br/> |
| FALSE  <br/> | Blatt nicht vergrößern.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die Zelle ResizePage anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ResizePage  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ResizePage-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOResizePage** <br/> |
   

