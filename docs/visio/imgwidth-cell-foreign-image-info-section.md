---
title: Zelle "ImgWidth" (Abschnitt "Foreign Image Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm460
ms.localizationpriority: medium
ms.assetid: b57fb962-0b3e-f2e5-3b88-3edf33e40496
description: 'Definiert die Breite des Objektbilds innerhalb seines Rahmens. Die Standardformel lautet:'
ms.openlocfilehash: d09728bcefe1b3f8f795d53cf03b7c09f173e51c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554607"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a>Zelle "ImgWidth" (Abschnitt "Foreign Image Info")

Definiert die Breite des Objektbilds innerhalb seines Rahmens. Die Standardformel lautet:
  
= Breite \* 1
  
Beim Zuschneiden des Objekts ändert sich der Faktor, mit dem die Breite multipliziert wird.
  
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle "ImgWidth" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ImgWidth  <br/> |
   
Um einen Verweis auf die Zelle "ImgWidth" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowForeign** <br/> |
| Zellenindex:  <br/> |**visFrgnImgWidth** <br/> |
   

