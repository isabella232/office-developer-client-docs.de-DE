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
ms.openlocfilehash: 22b9366b750a85a76498b83880aac2b9b974e1ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415040"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a>Zelle "ConLineJumpDirX" (Abschnitt "Shape Layout")

Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem horizontalen dynamischen Verbinder für ein Shape auftreten.
  
|**Wert**|**Liniensprungrichtung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Zeichenblattstandard  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | Nach oben  <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | Nach unten  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie die standardmäßige horizontale Richtung für *alle* Verbinder auf einem Zeichenblatt festlegen möchten, verwenden Sie die Zelle Zelle PageLineJumpDirX im Abschnitt Seiten Layout. 
  
Wenn Sie einen Verweis auf die Zelle Zelle ConLineJumpDirX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle ConLineJumpDirX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ConLineJumpDirX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
| Zellenindex:  <br/> |**visSLOJumpDirX** <br/> |
   

