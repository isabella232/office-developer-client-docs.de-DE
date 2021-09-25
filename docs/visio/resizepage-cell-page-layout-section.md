---
title: Zelle "ResizePage" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
ms.localizationpriority: medium
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: Bestimmt, ob die Seite vergrößert werden soll, um die Zeichnung mit einzuschließen, nachdem Shapes mithilfe des Dialogfelds Layout konfigurieren ausgerichtet wurden (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu anordnen, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 77fd339dd21c7f8111a7359ed8d293ddeee1111d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623075"
---
# <a name="resizepage-cell-page-layout-section"></a>Zelle "ResizePage" (Abschnitt "Page Layout")

Bestimmt, ob das Zeichenblatt vergrößert werden soll, um die Zeichnung einzuschließen, nachdem Shapes mithilfe des Dialogfelds **Layout konfigurieren** erstellt wurden (klicken Sie auf der Registerkarte **"Entwurf"** in der Gruppe **"Layout"** auf **"Seite neu anordnen"** und dann auf **"Weitere Layoutoptionen").**
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Blatt vergrößern.  <br/> |
| FALSE  <br/> | Blatt nicht vergrößern.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie Folgendes, um einen Verweis auf die Zelle "ResizePage" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ResizePage  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ResizePage anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOResizePage** <br/> |
   

