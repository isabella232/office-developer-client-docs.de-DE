---
title: Zelle "VerticalAlign" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
localization_priority: Normal
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: Definiert die vertikale Ausrichtung von Text in einem Textblock.
ms.openlocfilehash: cfd34f17eec597c306b69f76929877013b39015e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798391"
---
# <a name="verticalalign-cell-text-block-format-section"></a>Zelle "VerticalAlign" (Abschnitt "Text Block Format")

Definiert die vertikale Ausrichtung von Text in einem Textblock.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Oben  <br/> |**visVertTop** <br/> |
| 1  <br/> | Mitte  <br/> |**visVertMiddle** <br/> |
| 2  <br/> | Unten  <br/> |**visVertBottom** <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle VerticalAlign nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | VerticalAlign  <br/> |
   
Wenn Sie einen Verweis auf die Zelle VerticalAlign aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowText** <br/> |
| Zellenindex:  <br/> |**visTxtBlkVerticalAlign** <br/> |
   

