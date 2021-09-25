---
title: Zelle "CtrlAsInput" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1225
ms.localizationpriority: medium
ms.assetid: c6fd0aba-7c33-b77f-207b-ba704b3e0756
description: Legt die übergeordneten Shapes bei Verwendung von Shapes mit Steuerpunkten fest. Mithilfe dieser Zelle wird das Verhalten aller Shapes auf dem Zeichenblatt festgelegt.
ms.openlocfilehash: c662407838baa7276e7fedb23c1f5ff63821c855
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608347"
---
# <a name="ctrlasinput-cell-page-layout-section"></a>Zelle "CtrlAsInput" (Abschnitt "Page Layout")

Legt die übergeordneten Shapes bei Verwendung von Shapes mit Steuerpunkten fest. Mithilfe dieser Zelle wird das Verhalten aller Shapes auf dem Zeichenblatt festgelegt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Legt das mit dem Steuerpunkt verbundene Shape als das übergeordnete Element fest.  <br/> |
| FALSE  <br/> | Standard. Legt das Shape, in dem der Steuerpunkt enthalten ist, als das übergeordnete Element fest.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie Folgendes, um einen Verweis auf die Zelle CTrlAsInput anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | StrgAsInput  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle CTrlAsInput anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOCtrlAsInput** <br/> |
   

