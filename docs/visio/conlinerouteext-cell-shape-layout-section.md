---
title: Zelle "ConLineRouteExt" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50110
localization_priority: Normal
ms.assetid: cafd7589-1c94-b9bc-b1a6-40f7c15fba71
description: Bestimmt die Darstellung eines Verbinders.
ms.openlocfilehash: 19fe948daf7aa3d67db858849ecb2b15f40ba02d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434613"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a>Zelle "ConLineRouteExt" (Abschnitt "Shape Layout")

Bestimmt die Darstellung eines Verbinders.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Standard, Zeichenblatteinstellung verwenden  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Straight  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Gekrümmt  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die Zelle ConLineRouteExt anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ConLineRouteExt  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ConLineRouteExt-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
| Zellenindex:  <br/> |**visSLOLineRouteExt** <br/> |
   

