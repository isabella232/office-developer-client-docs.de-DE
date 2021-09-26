---
title: Zelle "Can Glue" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251287
ms.localizationpriority: medium
ms.assetid: 1c4c4ae2-b3fa-ed45-c6e5-22bedb2523db
description: Legt fest, ob ein Steuerpunkt an andere Shapes geklebt werden kann.
ms.openlocfilehash: 751a9b28351965b0239c34b6195e75f89d5f1b7c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613128"
---
# <a name="can-glue-cell-controls-section"></a>Zelle "Can Glue" (Abschnitt "Controls")

Legt fest, ob ein Steuerpunkt an andere Shapes geklebt werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Steuerpunkt kann geklebt werden.  <br/> |
| FALSE  <br/> | Steuerpunkt kann nicht geklebt werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um einen Verweis auf die Zelle "Can Glue" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name*  . CanGluewhere-Steuerelemente.  *Name*  ist der Name der Steuerelementzeile.  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Can Glue anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionControls** <br/> |
| Zeilenindex:  <br/> |**visRowControl**  +   *i* where *i* = 0, 1, 2, ...  <br/> |
| Zellenindex:  <br/> |**visCtlGlue** <br/> |
   

