---
title: Zelle "PageLineJumpDirY" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm770
localization_priority: Normal
ms.assetid: f73cc157-b332-279b-f7cf-d5a090bc09a4
description: Bestimmt die Richtung von Liniensprüngen auf vertikalen dynamischen Verbindern auf dem Zeichenblatt, für die Sie keine lokale Liniensprungrichtung festgelegt haben.
ms.openlocfilehash: 21ad1d95fd83780f31778dbc8bb70f9bdb4b922d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414676"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a>Zelle "PageLineJumpDirY" (Abschnitt "Page Layout")

Bestimmt die Richtung von Liniensprüngen auf vertikalen dynamischen Verbindern auf dem Zeichenblatt, für die Sie keine lokale Liniensprungrichtung festgelegt haben.
  
|**Wert**|**Liniensprungrichtung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Standard, nach oben oder die Einstellung des Zeichenblatts für Shapes  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | Nach links  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | Nach rechts  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle PageLineJumpDirY anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PageLineJumpDirY  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PageLineJumpDirY nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOJumpDirY** <br/> |
   

