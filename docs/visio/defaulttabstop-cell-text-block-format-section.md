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
ms.openlocfilehash: 1ae923f6373b9cee76238b1fb27ec5eb3acb43ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360270"
---
# <a name="defaulttabstop-cell-text-block-format-section"></a>Zelle "DefaultTabstop" (Abschnitt "Text Block Format")

Bestimmt das Intervall der Standardtabstopps in einem Textblock. 
  
## <a name="remarks"></a>Bemerkungen

Der Standardwert ist 1,27 cm für Dokumente, die unter Verwendung britischer Maßeinheiten erstellt wurden, oder 1,5 cm für Dokumente, die in metrischen Maßeinheiten erstellt wurden.
  
Wenn Sie einen Verweis auf die Zelle DefaultTabstop aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |DefaultTabstop  <br/> |
   
Wenn Sie einen Verweis auf die Zelle DefaultTabstop aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowText** <br/> |
|Zellenindex:  <br/> |**visTxtBlkDefaultTabStop** <br/> |
   

