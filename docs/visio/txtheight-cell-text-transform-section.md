---
title: Zelle "TxtHeight" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
localization_priority: Normal
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: 'Definiert die Höhe eines Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: e9495eef837a61fa9b7ecb2b242fdabc5df30080
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798326"
---
# <a name="txtheight-cell-text-transform-section"></a>Zelle "TxtHeight" (Abschnitt "Text Transform")

Definiert die Höhe eines Textblocks. Die Standardformel lautet:
  
= Höhe \* 1
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle TxtHeight nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TxtHeight  <br/> |
   
Wenn Sie einen Verweis auf die Zelle TxtHeight aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowTextXForm** <br/> |
| Zellenindex:  <br/> |**visXFormHeight** <br/> |
   

