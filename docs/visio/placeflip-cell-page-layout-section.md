---
title: Zelle "PlaceFlip" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253251
ms.localizationpriority: medium
ms.assetid: df014b98-cfd5-b6d3-4b8a-b0acb3b94412
description: Legt fest, wie platzierbare Shapes auf einem Zeichenblatt gekippt und/oder gedreht werden, wenn Sie das Dialogfeld Layout konfigurieren verwenden (klicken Sie dazu auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu anordnen, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 10165312a0ad4c595a58f4ab94d319b0a3d61d29
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598430"
---
# <a name="placeflip-cell-page-layout-section"></a>Zelle "PlaceFlip" (Abschnitt "Page Layout")

Legt fest, wie platzierbare Shapes auf einem Zeichenblatt gekippt und/oder gedreht werden, wenn Sie das Dialogfeld **Layout konfigurieren** verwenden (klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu anordnen**, und klicken Sie dann auf **Weitere Layoutoptionen**).
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |Standard. Nicht kippen.  <br/> |**visLOFlipDefault** <br/> |
|&amp;H1  <br/> |Horizontal kippen.  <br/> |**visLOFlipX** <br/> |
|&amp;H2  <br/> |Vertikal kippen.  <br/> |**visLOFlipY** <br/> |
|&amp;H4  <br/> |In 90-Grad-Schritten kippen.  <br/> |**visLOFlipRotate** <br/> |
|&amp;H8  <br/> |Nicht kippen.  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert in der Zelle PlaceFlip hilft bei der Ausrichtung eines platzierbaren Shapes in Richtung des nächsten platzierbaren Shapes, mit dem es verbunden ist. Dieser Wert wird normalerweise verwendet, wenn Sie Zeichnungen ausrichten, die statischen Kleber verwenden.
  
Wenn Sie dieses Verhalten für ein bestimmtes Shape festlegen möchten, verwenden Sie die Zelle ShapePlaceFlip im Abschnitt Shape Layout.
  
Um einen Verweis auf die Zelle PlaceFlip anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PlaceFlip  <br/> |
   
Um einen Verweis auf die Zelle PlaceFlip anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOPlaceFlip** <br/> |
   

