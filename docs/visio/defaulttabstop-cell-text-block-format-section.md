---
title: Zelle "DefaultTabstop" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm220
localization_priority: Normal
ms.assetid: 3b3e458a-206c-8699-8bf7-da80f4350706
description: Bestimmt das Intervall der Standardtabstopps in einem Textblock.
ms.openlocfilehash: 2b9c2c5b03da98b30e338a250b56091479067955
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796837"
---
# <a name="defaulttabstop-cell-text-block-format-section"></a>DefaultTabstop Cell (Text Block Format Section)

Bestimmt das Intervall der Standardtabstopps in einem Textblock. 
  
## <a name="remarks"></a>Bemerkungen

Der Standardwert ist 1,27 cm für Dokumente, die unter Verwendung britischer Maßeinheiten erstellt wurden, oder 1,5 cm für Dokumente, die in metrischen Maßeinheiten erstellt wurden.
  
Wenn Sie einen Verweis auf die Zelle DefaultTabstop aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |DefaultTabstop  <br/> |
   
Wenn Sie einen Verweis auf die Zelle DefaultTabstop aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowText** <br/> |
|Zellenindex:  <br/> |**visTxtBlkDefaultTabStop** <br/> |
   

