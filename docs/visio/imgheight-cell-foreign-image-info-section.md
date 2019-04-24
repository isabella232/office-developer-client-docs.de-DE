---
title: Zelle "ImgHeight" (Abschnitt "Foreign Image Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
localization_priority: Normal
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: 'Definiert die Höhe des Bilds des Objekts innerhalb seines Rahmens. Die Standardformel lautet:'
ms.openlocfilehash: 956bc478604fd19d8dfdbb7079e092e9e8a16e7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344933"
---
# <a name="imgheight-cell-foreign-image-info-section"></a>Zelle "ImgHeight" (Abschnitt "Foreign Image Info")

Definiert die Höhe des Bilds des Objekts innerhalb seines Rahmens. Die Standardformel lautet:
  
= Höhe \* 1
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle ImgHeight aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle ImgHeight  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ImgHeight aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowForeign** <br/> |
| Zellenindex:  <br/> |**visFrgnImgHeight** <br/> |
   

