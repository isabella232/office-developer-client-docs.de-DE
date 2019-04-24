---
title: Zelle "Blur" (Abschnitt "Image Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm115
localization_priority: Normal
ms.assetid: 8b077cdb-6036-4f77-dc20-a476bb75b0f7
description: Eine Bitmapgrafik wird verwischt oder weichgezeichnet. Der Standardwert ist 0 %.
ms.openlocfilehash: 599810d126c853e37552045d0ef83cb580606ae2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348979"
---
# <a name="blur-cell-image-properties-section"></a>Zelle "Blur" (Abschnitt "Image Properties")

Eine Bitmapgrafik wird verwischt oder weichgezeichnet. Der Standardwert ist 0 %.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle "Blur" aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Weichzeichnen  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Unschärfe aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowImage** <br/> |
| Zellenindex:  <br/> |**visImageBlur** <br/> |
   

