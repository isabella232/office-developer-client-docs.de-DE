---
title: Zelle "ConLineJumpDirX" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem horizontalen dynamischen Verbinder für ein Shape auftreten.
ms.openlocfilehash: 396830d0da22c15f036f95808b3a94c33e9dc5bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796704"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a>ConLineJumpDirX Cell (Shape Layout Section)

Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem horizontalen dynamischen Verbinder für ein Shape auftreten.
  
|**Wert**|**Liniensprungrichtung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Zeichenblattstandard  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | Nach oben  <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | Nach unten  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Zum Festlegen der horizontaler Richtung für *Alle* Verbinder auf einem Zeichenblatt springt, verwenden Sie die Zelle PageLineJumpDirX im Abschnitt Page Layout. 
  
Wenn Sie einen Verweis auf die Zelle ConLineJumpDirX aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ConLineJumpDirX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ConLineJumpDirX aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
| Zellenindex:  <br/> |**visSLOJumpDirX** <br/> |
   

