---
title: Zelle "Sharpen" (Abschnitt "Image Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm910
localization_priority: Normal
ms.assetid: aa2bebfc-a6bb-a6b3-3ae9-8553f96b5738
description: Schärft eine Bitmapgrafik. Der Standardwert ist 0 %. Beim Scharfzeichnen einer Grafik wird diese durch Erhöhen des Kontrasts angrenzender Pixel fokussiert.
ms.openlocfilehash: fbc66f8c88cde67ad1f259f8392f6d3bd0457be7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798068"
---
# <a name="sharpen-cell-image-properties-section"></a>Sharpen Cell (Image Properties Section)

Schärft eine Bitmapgrafik. Der Standardwert ist 0 %. Beim Scharfzeichnen einer Grafik wird diese durch Erhöhen des Kontrasts angrenzender Pixel fokussiert.
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle Sharpen nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Sharpen  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Sharpen aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowImage** <br/> |
| Zellenindex:  <br/> |**visImageSharpen** <br/> |
   

