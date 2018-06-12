---
title: Zelle "Brightness" (Abschnitt "Image Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251608
localization_priority: Normal
ms.assetid: 5bb1cc81-f3fd-a835-1449-233dbd1a62b6
description: Passt die Helligkeit einer Bitmapgrafik an. Verringern Sie die Helligkeit einer Grafik durch Eingabe eines Werts zwischen 0 % und 49 %, oder steigern Sie die Helligkeit durch Eingabe eines Werts zwischen 51 % und 100 %. Der Standardwert lautet 50 %.
ms.openlocfilehash: 688a6cacfa9100ad116b9bf06926194c24712219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796540"
---
# <a name="brightness-cell-image-properties-section"></a>Brightness Cell (Image Properties Section)

Passt die Helligkeit einer Bitmapgrafik an. Verringern Sie die Helligkeit einer Grafik durch Eingabe eines Werts zwischen 0 % und 49 %, oder steigern Sie die Helligkeit durch Eingabe eines Werts zwischen 51 % und 100 %. Der Standardwert lautet 50 %.
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle Brightness nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Brightness  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Brightness aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowImage** <br/> |
| Zellenindex:  <br/> |**visImageBrightness** <br/> |
   

