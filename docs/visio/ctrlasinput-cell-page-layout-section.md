---
title: Zelle "CtrlAsInput" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1225
localization_priority: Normal
ms.assetid: c6fd0aba-7c33-b77f-207b-ba704b3e0756
description: Legt die übergeordneten Shapes bei Verwendung von Shapes mit Steuerpunkten fest. Mithilfe dieser Zelle wird das Verhalten aller Shapes auf dem Zeichenblatt festgelegt.
ms.openlocfilehash: a530c48156043bec0cd58d79aead1a403c17ddce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422621"
---
# <a name="ctrlasinput-cell-page-layout-section"></a>Zelle "CtrlAsInput" (Abschnitt "Page Layout")

Legt die übergeordneten Shapes bei Verwendung von Shapes mit Steuerpunkten fest. Mithilfe dieser Zelle wird das Verhalten aller Shapes auf dem Zeichenblatt festgelegt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Legt das mit dem Steuerpunkt verbundene Shape als das übergeordnete Element fest.  <br/> |
| FALSE  <br/> | Standard. Legt das Shape, in dem der Steuerpunkt enthalten ist, als das übergeordnete Element fest.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle StrgAsInput anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | STRGAsInput  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die StrgAsInput-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOCtrlAsInput** <br/> |
   

