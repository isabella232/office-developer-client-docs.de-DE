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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327104"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a>Zelle "ConLineRouteExt" (Abschnitt "Shape Layout")

Bestimmt die Darstellung eines Verbinders.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Standard, Zeichenblatteinstellung verwenden  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Gerade  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Gebogene  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle ConLineRouteExt aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle ConLineRouteExt  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ConLineRouteExt aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
| Zellenindex:  <br/> |**visSLOLineRouteExt** <br/> |
   

