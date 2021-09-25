---
title: Zelle "ResizeMode" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
ms.localizationpriority: medium
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: Zeigt die aktuelle Einstellung für das Größenänderungsverhalten in Bezug auf das Shape an.
ms.openlocfilehash: 5893e01d7d66d7c9dfad6544c83b7299709ccf1c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607801"
---
# <a name="resizemode-cell-shape-transform-section"></a>Zelle "ResizeMode" (Abschnitt "Shape Transform")

Zeigt die aktuelle Einstellung für das Größenänderungsverhalten in Bezug auf das Shape an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Einstellung der Gruppe verwenden.  <br/> |**visXFormResizeDontCare** <br/> |
|1  <br/> |Nur neu positionieren.  <br/> |**visXFormResizeSpread** <br/> |
|2  <br/> |Mit Gruppe skalieren.  <br/> |**visXFormResizeScale** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können diesen Wert auch auf der Registerkarte **"Verhalten"** im Dialogfeld **"Verhalten"** festlegen (klicken Sie auf der Registerkarte ["Entwicklertools"](run-in-developer-mode-display-the-developer-tab.md)in der Gruppe **"Shape-Entwurf"** auf **"Verhalten").** Um einen Verweis auf die Zelle "ResizeMode" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Resizemode  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ResizeMode anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
|Zellenindex:  <br/> |**visXFormResizeMode** <br/> |
   

