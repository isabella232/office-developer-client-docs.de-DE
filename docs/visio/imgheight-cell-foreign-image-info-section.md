---
title: Zelle "ImgHeight" (Abschnitt "Foreign Image Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
ms.localizationpriority: medium
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: 'Definiert die Höhe des Bilds des Objekts innerhalb seines Rahmens. Die Standardformel lautet:'
ms.openlocfilehash: 927b614e7e0b8113c96f7965c5f9b84b9a6c5b78
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628164"
---
# <a name="imgheight-cell-foreign-image-info-section"></a>Zelle "ImgHeight" (Abschnitt "Foreign Image Info")

Definiert die Höhe des Bilds des Objekts innerhalb seines Rahmens. Die Standardformel lautet:
  
= Höhe \* 1
  
## <a name="remarks"></a>Bemerkungen

Um einen Verweis auf die Zelle "ImgHeight" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ImgHeight  <br/> |
   
Um einen Verweis auf die Zelle "ImgHeight" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowForeign** <br/> |
| Zellenindex:  <br/> |**visFrgnImgHeight** <br/> |
   

