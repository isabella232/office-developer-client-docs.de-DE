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
ms.openlocfilehash: e519cf6e5a168b64b4bc8aa083843163a47525ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415922"
---
# <a name="sharpen-cell-image-properties-section"></a>Zelle "Sharpen" (Abschnitt "Image Properties")

Schärft eine Bitmapgrafik. Der Standardwert ist 0 %. Beim Scharfzeichnen einer Grafik wird diese durch Erhöhen des Kontrasts angrenzender Pixel fokussiert.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle schärfen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | "Sharpen  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Scharfzeichnen aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowImage** <br/> |
| Zellenindex:  <br/> |**visImageSharpen** <br/> |
   

