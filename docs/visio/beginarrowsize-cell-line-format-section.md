---
title: Zelle "BeginArrowSize" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251629
localization_priority: Normal
ms.assetid: bfddb829-6e13-7d74-b9b9-2cb5c0937bae
description: Bestimmt die Pfeilspitzengröße am Linienanfang.
ms.openlocfilehash: b38e4a0685fce6d7f4aea2192ed123665eacf40a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796419"
---
# <a name="beginarrowsize-cell-line-format-section"></a>BeginArrowSize Cell (Line Format Section)

Bestimmt die Pfeilspitzengröße am Linienanfang.
  
|**Wert**|**Size**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Sehr klein  <br/> |**visArrowSizeVerySmall** <br/> |
| 1  <br/> | Klein  <br/> |**visArrowSizeSmall** <br/> |
| 2  <br/> | Mittel  <br/> |**visArrowSizeMedium** <br/> |
| 3  <br/> | Groß  <br/> |**visArrowSizeLarge** <br/> |
| 4  <br/> | Sehr groß  <br/> |**visArrowSizeVeryLarge** <br/> |
| 5  <br/> | Jumbo  <br/> |**visArrowSizeJumbo** <br/> |
| 6  <br/> | Kolossal  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können die Pfeilspitzengröße auch im Dialogfeld **Linie** festlegen. 
  
Wenn Sie einen Verweis auf die Zelle BeginArrowSize aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | BeginArrowSize  <br/> |
   
Wenn Sie einen Verweis auf die Zelle BeginArrowSize aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLine** <br/> |
| Zellenindex:  <br/> |**visLineBeginArrowSize** <br/> |
   

