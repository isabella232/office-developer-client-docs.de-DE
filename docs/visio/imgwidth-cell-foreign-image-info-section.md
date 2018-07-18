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
ms.openlocfilehash: 3aab65d27d426287060f7572dad15174acb93199
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797195"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a>ImgWidth Cell (Foreign Image Info Section)

Definiert die Breite des Objektbilds innerhalb seines Rahmens. Die Standardformel lautet:
  
= Breite \* 1
  
Beim Zuschneiden des Objekts ändert sich der Faktor, mit dem die Breite multipliziert wird.
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle ImgWidth aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ImgWidth  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ImgWidth aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowForeign** <br/> |
| Zellenindex:  <br/> |**visFrgnImgWidth** <br/> |
   

