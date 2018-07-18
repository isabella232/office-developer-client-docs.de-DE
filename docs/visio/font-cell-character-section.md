---
title: Zelle "Font" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm390
localization_priority: Normal
ms.assetid: 935760a9-307e-90bc-c301-d04283d97427
description: Stellt die Nummer der Schriftart dar, die zum Formatieren des Texts verwendet wird. Schriftartnummern können abhängig von den auf Ihrem System installierten Schriftarten variieren. Die Nummer 0 stellt die Standardschriftart dar, bei der es sich i. A. um die Schriftart Arial handelt.
ms.openlocfilehash: cbbf2a2400c995e0cbc217c1161fbd18f7459b28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797033"
---
# <a name="font-cell-character-section"></a>Font Cell (Character Section)

Stellt die Nummer der Schriftart dar, die zum Formatieren des Texts verwendet wird. Schriftartnummern können abhängig von den auf Ihrem System installierten Schriftarten variieren. Die Nummer 0 stellt die Standardschriftart dar, bei der es sich i. A. um die Schriftart Arial handelt.
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle Font aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Char.Font [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Font aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
| Zeilenindex:  <br/> |**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCharacterFont** <br/> |
   

