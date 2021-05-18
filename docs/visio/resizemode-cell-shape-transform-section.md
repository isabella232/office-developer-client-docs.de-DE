---
title: Zelle "ResizeMode" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
localization_priority: Normal
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: Zeigt die aktuelle Einstellung für das Größenänderungsverhalten in Bezug auf das Shape an.
ms.openlocfilehash: 7e9080fcd4604e2dbdc1dae31992f05e5b512213
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421963"
---
# <a name="resizemode-cell-shape-transform-section"></a>Zelle "ResizeMode" (Abschnitt "Shape Transform")

Zeigt die aktuelle Einstellung für das Größenänderungsverhalten in Bezug auf das Shape an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Einstellung der Gruppe verwenden.  <br/> |**visXFormResizeDontCare** <br/> |
|1  <br/> |Nur neu positionieren.  <br/> |**visXFormResizeSpread** <br/> |
|2  <br/> |Mit Gruppe skalieren.  <br/> |**visXFormResizeScale** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können diesen Wert  auch auf der Registerkarte Verhalten [](run-in-developer-mode-display-the-developer-tab.md)im Dialogfeld Verhalten festlegen (klicken Sie auf der Registerkarte Entwickler in der **Gruppe Shape-Entwurf** auf  **Verhalten**). Um einen Verweis auf die Zelle ResizeMode anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ResizeMode  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ResizeMode nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
|Zellenindex:  <br/> |**visXFormResizeMode** <br/> |
   

