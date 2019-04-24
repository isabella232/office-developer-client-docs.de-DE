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
ms.openlocfilehash: ae1390d2db3adad86a8afcbeaff88172a841d030
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338024"
---
# <a name="brightness-cell-image-properties-section"></a>Zelle "Brightness" (Abschnitt "Image Properties")

Passt die Helligkeit einer Bitmapgrafik an. Verringern Sie die Helligkeit einer Grafik durch Eingabe eines Werts zwischen 0 % und 49 %, oder steigern Sie die Helligkeit durch Eingabe eines Werts zwischen 51 % und 100 %. Der Standardwert lautet 50 %.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Brightness aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Helligkeit  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "Brightness" aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowImage** <br/> |
| Zellenindex:  <br/> |**visImageBrightness** <br/> |
   

