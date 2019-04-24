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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344723"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a>Zelle "ImgWidth" (Abschnitt "Foreign Image Info")

Definiert die Breite des Objektbilds innerhalb seines Rahmens. Die Standardformel lautet:
  
= Breite \* 1
  
Beim Zuschneiden des Objekts ändert sich der Faktor, mit dem die Breite multipliziert wird.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle ImgWidth aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle ImgWidth  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ImgWidth aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowForeign** <br/> |
| Zellenindex:  <br/> |**visFrgnImgWidth** <br/> |
   

