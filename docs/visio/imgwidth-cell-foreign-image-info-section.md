---
title: Zelle "ImgWidth" (Abschnitt "Foreign Image Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm460
localization_priority: Normal
ms.assetid: b57fb962-0b3e-f2e5-3b88-3edf33e40496
description: 'Definiert die Breite des Objektbilds innerhalb seines Rahmens. Die Standardformel lautet:'
ms.openlocfilehash: 9da5e06a7fbf6ae77a49fb0410aefb406e2afecb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422831"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a>Zelle "ImgWidth" (Abschnitt "Foreign Image Info")

Definiert die Breite des Objektbilds innerhalb seines Rahmens. Die Standardformel lautet:
  
= Breite \* 1
  
Beim Zuschneiden des Objekts ändert sich der Faktor, mit dem die Breite multipliziert wird.
  
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die ImgWidth-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ImgWidth  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ImgWidth-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowForeign** <br/> |
| Zellenindex:  <br/> |**visFrgnImgWidth** <br/> |
   

