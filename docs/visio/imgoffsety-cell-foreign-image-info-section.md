---
title: Zelle "ImgOffsetY" (Abschnitt "Foreign Image Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm455
localization_priority: Normal
ms.assetid: 3b2991aa-4722-fe3b-39c5-02d38c4c7efc
description: Bestimmt der Abstand das Objekt vertikal vom Ursprung des Rahmens des Objekts entfernt wird. Der Standardwert ist 0. Durch Bearbeitung des Objekts mit der Zuschneide-Tool Änderungen dieser Wert.
ms.openlocfilehash: 2930aa092a2b776ceb0c9c4677f7e5da7f5dcdda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797189"
---
# <a name="imgoffsety-cell-foreign-image-info-section"></a>ImgOffsetY Cell (Foreign Image Info Section)

Bestimmt der Abstand das Objekt vertikal vom Ursprung des Rahmens des Objekts entfernt wird. Der Standardwert ist 0. Durch Bearbeitung des Objekts mit der **Zuschneide** -Tool Änderungen dieser Wert. 
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle ImgOffsetY nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ImgOffsetY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ImgOffsetY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowForeign** <br/> |
| Zellenindex:  <br/> |**visFrgnImgOffsetY** <br/> |
   

