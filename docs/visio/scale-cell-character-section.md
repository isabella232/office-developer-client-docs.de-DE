---
title: Zelle "Scale" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm870
localization_priority: Normal
ms.assetid: d6fe2574-b719-f38e-b1f1-592a812f1682
description: Steuert die Schriftartbreite. Der Standardwert für diese Zelle ist 100%.
ms.openlocfilehash: fedbc0aec23320d03ca358f34babda56eaab31e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797971"
---
# <a name="scale-cell-character-section"></a>Zelle "Scale" (Abschnitt "Character")

Steuert die Schriftartbreite. Der Standardwert für diese Zelle ist 100%.
  
## <a name="remarks"></a>Bemerkungen

Legen Sie einen Prozentsatz zwischen 1% und 99% fest, um die Schriftartbreite zu reduzieren. Legen Sie einen Prozentsatz zwischen 101% und 600% fest, um die Schriftartbreite zu erhöhen.
  
Sie können den Wert dieser Zelle auch festlegen, indem Sie das Dialogfeld **Text** verwenden (klicken Sie auf der Registerkarte **Start** auf den Pfeil neben **Schriftart** ). 
  
Wenn Sie einen Verweis auf die Zelle Scale nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Char.FontScale [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Scale aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
|Zeilenindex:  <br/> |**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCharacterFontScale** <br/> |
   

