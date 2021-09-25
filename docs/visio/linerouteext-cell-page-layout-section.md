---
title: Zelle "LineRouteExt" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50115
ms.localizationpriority: medium
ms.assetid: 3d16b8b3-601b-c10b-68a8-ffd47251306f
description: Legt das standardmäßige Erscheinungsbild für sämtliche Verbinder auf einem Zeichenblatt fest.
ms.openlocfilehash: 37bcf569b4a095ed1b3e08823db1673ef5cc95cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615886"
---
# <a name="linerouteext-cell-page-layout-section"></a>Zelle "LineRouteExt" (Abschnitt "Page Layout")

Legt das standardmäßige Erscheinungsbild für sämtliche Verbinder auf einem Zeichenblatt fest.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Standardeinstellung (gerade)  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Gerade  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Gebogene  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie zum Abrufen eines Verweises auf die Zelle "LineRouteExt" anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LineRouteExt  <br/> |
   
Um einen Verweis auf die Zelle "LineRouteExt" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOLineRouteExt** <br/> |
   

