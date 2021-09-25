---
title: Zelle "ConLineRouteExt" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50110
ms.localizationpriority: medium
ms.assetid: cafd7589-1c94-b9bc-b1a6-40f7c15fba71
description: Bestimmt die Darstellung eines Verbinders.
ms.openlocfilehash: f3bba289b4b4f4dc880694b40b8bf835f7cdc321
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577969"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a>Zelle "ConLineRouteExt" (Abschnitt "Shape Layout")

Bestimmt die Darstellung eines Verbinders.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Standard, Zeichenblatteinstellung verwenden  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Gerade  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Gebogene  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle "ConLineRouteExt" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ConLineRouteExt  <br/> |
   
Verwenden Sie zum Abrufen eines Verweises auf die Zelle "ConLineRouteExt" anhand des Indexes eines Programms die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
| Zellenindex:  <br/> |**visSLOLineRouteExt** <br/> |
   

