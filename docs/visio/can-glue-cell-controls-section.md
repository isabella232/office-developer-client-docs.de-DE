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
ms.openlocfilehash: 2f5e65ab72c584f88b56e273b0d73abf969a6588
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423293"
---
# <a name="can-glue-cell-controls-section"></a>Zelle "Can Glue" (Abschnitt "Controls")

Legt fest, ob ein Steuerpunkt an andere Shapes geklebt werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Steuerpunkt kann geklebt werden.  <br/> |
| FALSE  <br/> | Steuerpunkt kann nicht geklebt werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Bezug auf die Zelle can Glue aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name* . CanGluewhere-Steuerelemente.  *Name* ist der Name der Zeile Controls.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle can Glue aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionControls** <br/> |
| Zeilenindex:  <br/> |**visRowControl** +  *i* , wobei *i* = 0, 1, 2,...  <br/> |
| Zellenindex:  <br/> |**visCtlGlue** <br/> |
   

