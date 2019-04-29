---
title: Zelle "FlipX" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251197
localization_priority: Normal
ms.assetid: 8d4f5e14-4f17-05a6-4092-5a102c9dc85f
description: Gibt an, ob das Shape horizontal gekippt wurde.
ms.openlocfilehash: b7a4a15e5a7759eddcda3ec391a81f14df545691
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415950"
---
# <a name="flipx-cell-shape-transform-section"></a>Zelle "FlipX" (Abschnitt "Shape Transform")

Gibt an, ob das Shape horizontal gekippt wurde.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Das Shape wurde horizontal gekippt.  <br/> |
| FALSE  <br/> | Das Shape wurde nicht horizontal gekippt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle FlipX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle FlipX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle FlipX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
| Zellenindex:  <br/> |**visXFormFlipX** <br/> |
   

