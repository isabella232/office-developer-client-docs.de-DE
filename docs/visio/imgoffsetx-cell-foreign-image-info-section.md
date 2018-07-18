---
title: Zelle "ImgOffsetX" (Abschnitt "Foreign Image Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251308
localization_priority: Normal
ms.assetid: c079fb10-4db7-4657-75d2-2fb953c86670
description: Bestimmt den Abstand, den das Objekt horizontal vom Ursprung des Rahmens des Objekts entfernt ist. Der Standardwert ist 0. Durch Bearbeitung des Objekts mit dem Zuschneidetool wird dieser Wert geändert.
ms.openlocfilehash: dda385b2157e48baec2b21c6da741b31d05c3291
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797196"
---
# <a name="imgoffsetx-cell-foreign-image-info-section"></a>ImgOffsetX Cell (Foreign Image Info Section)

Bestimmt der Abstand des Objekts horizontal vom Ursprung des Rahmens des Objekts entfernt wird. Der Standardwert ist 0. Durch Bearbeitung des Objekts mit der **Zuschneide** -Tool Änderungen dieser Wert. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle ImgOffsetX aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ImgOffsetX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ImgOffsetX aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowForeign** <br/> |
| Zellenindex:  <br/> |**visFrgnImgOffsetX** <br/> |
   

