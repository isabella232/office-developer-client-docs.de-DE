---
title: Zelle "Can Glue" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251287
localization_priority: Normal
ms.assetid: 1c4c4ae2-b3fa-ed45-c6e5-22bedb2523db
description: Legt fest, ob ein Steuerpunkt an andere Shapes geklebt werden kann.
ms.openlocfilehash: c7b6764e25deab3345b7b3cecd6cf12dde74a84c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796553"
---
# <a name="can-glue-cell-controls-section"></a>Can Glue Cell (Controls Section)

Legt fest, ob ein Steuerpunkt an andere Shapes geklebt werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Steuerpunkt kann geklebt werden.  <br/> |
| FALSE  <br/> | Steuerpunkt kann nicht geklebt werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle Can Glue aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name* . CanGluewhere-Steuerelemente.  *Name* ist der Name der Zeile mit Steuerelementen.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Can Glue aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionControls** <br/> |
| Zeilenindex:  <br/> |**VisRowControl** +  *i* wobei *i* = 0, 1, 2,...  <br/> |
| Zellenindex:  <br/> |**visCtlGlue** <br/> |
   

