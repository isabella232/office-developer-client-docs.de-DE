---
title: Zelle "TextDirection" (Abschnitt "Text Block Format ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm995
localization_priority: Normal
ms.assetid: 1df3a50e-7ea5-9244-1286-c1d00c217a9a
description: Bestimmt die Richtung der Zeichen in einem Textblock.
ms.openlocfilehash: c238b6b2a47c968809869f8eb3e38b6f0db1dcad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798267"
---
# <a name="textdirection-cell-text-block-format-section"></a>TextDirection Cell (Text Block Format Section)

Bestimmt die Richtung der Zeichen in einem Textblock.
  
|**Wert**|**Direction**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Horizontal  <br/> |**visTxtBlkLeftToRight** <br/> |
| 1  <br/> | Vertikal  <br/> |**visTxtBlkTopToBottom** <br/> |
   
## <a name="remarks"></a>Hinweise

In der japanischen Ausgabe von Visio Version  5.0 wurde der Wert dieser Zelle in der Zelle VerticalText im Abschnitt Miscellaneous gespeichert.
  
Wenn Sie einen Verweis auf die Zelle TextDirection aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TextDirection  <br/> |
   
Wenn Sie einen Verweis auf die Zelle TextDirection aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowText** <br/> |
| Zellenindex:  <br/> |**visTxtBlkDirection** <br/> |
   

