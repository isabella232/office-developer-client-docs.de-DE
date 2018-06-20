---
title: Zelle "ConLineJumpDirY" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
localization_priority: Normal
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem vertikalen dynamischen Verbinder für ein Shape auftreten.
ms.openlocfilehash: 2d0c0964b52c9afbccc9cb507024825434702b6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796692"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a>ConLineJumpDirY Cell (Shape Layout Section)

Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem vertikalen dynamischen Verbinder für ein Shape auftreten.
  
|**Wert**|**Liniensprungrichtung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Zeichenblattstandard  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | Nach links  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | Nach rechts  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Hinweise

Zum Festlegen der vertikaler Richtung für *Alle* Verbinder auf einem Zeichenblatt springt, verwenden Sie die Zelle PageLineJumpDirY im Abschnitt Page Layout. 
  
Wenn Sie einen Verweis auf die Zelle ConLineJumpDirY nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ConLineJumpDirY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ConLineJumpDirY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
| Zellenindex:  <br/> |**visSLOJumpDirY** <br/> |
   

