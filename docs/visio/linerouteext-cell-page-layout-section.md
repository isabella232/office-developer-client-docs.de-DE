---
title: Zelle "LineRouteExt" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50115
localization_priority: Normal
ms.assetid: 3d16b8b3-601b-c10b-68a8-ffd47251306f
description: Legt das standardmäßige Erscheinungsbild für sämtliche Verbinder auf einem Zeichenblatt fest.
ms.openlocfilehash: 6daed2e06f7673e5a4ec97ec83dc31bad2766301
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410623"
---
# <a name="linerouteext-cell-page-layout-section"></a>Zelle "LineRouteExt" (Abschnitt "Page Layout")

Legt das standardmäßige Erscheinungsbild für sämtliche Verbinder auf einem Zeichenblatt fest.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Standardeinstellung (gerade)  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Straight  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Gekrümmt  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die Zelle LineRouteExt anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LineRouteExt  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LineRouteExt-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOLineRouteExt** <br/> |
   

