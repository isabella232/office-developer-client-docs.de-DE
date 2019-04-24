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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358982"
---
# <a name="linerouteext-cell-page-layout-section"></a>Zelle "LineRouteExt" (Abschnitt "Page Layout")

Legt das standardmäßige Erscheinungsbild für sämtliche Verbinder auf einem Zeichenblatt fest.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Standardeinstellung (gerade)  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Gerade  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Gebogene  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle LineRouteExt aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle LineRouteExt  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle LineRouteExt aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOLineRouteExt** <br/> |
   

