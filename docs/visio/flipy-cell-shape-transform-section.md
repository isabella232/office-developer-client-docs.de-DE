---
title: Zelle "FlipY" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251198
localization_priority: Normal
ms.assetid: 062022ff-e243-2540-becd-d9b969ce83ce
description: Gibt an, ob das Shape vertikal gekippt wurde.
ms.openlocfilehash: 44ea0341cda3655e8acc69e82e89acddac69b80d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346200"
---
# <a name="flipy-cell-shape-transform-section"></a>Zelle "FlipY" (Abschnitt "Shape Transform")

Gibt an, ob das Shape vertikal gekippt wurde.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Das Shape wurde vertikal gekippt.  <br/> |
| FALSE  <br/> | Das Shape wurde nicht vertikal gekippt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle FlipY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | FlipY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle FlipY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
| Zellenindex:  <br/> |**visXFormFlipY** <br/> |
   

