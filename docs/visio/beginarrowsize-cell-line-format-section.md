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
ms.openlocfilehash: 9c1288ced747c4e16090013cc043b040f1fbb59c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412282"
---
# <a name="beginarrowsize-cell-line-format-section"></a>Zelle "BeginArrowSize" (Abschnitt "Line Format")

Bestimmt die Pfeilspitzengröße am Linienanfang.
  
|**Wert**|**Größe**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Sehr klein  <br/> |**visArrowSizeVerySmall** <br/> |
| 1  <br/> | Small  <br/> |**visArrowSizeSmall** <br/> |
| 2  <br/> | Mittel  <br/> |**visArrowSizeMedium** <br/> |
| 3  <br/> | Large  <br/> |**visArrowSizeLarge** <br/> |
| 4   <br/> | Sehr groß  <br/> |**visArrowSizeVeryLarge** <br/> |
| 5   <br/> | Jumbo  <br/> |**visArrowSizeJumbo** <br/> |
| 6   <br/> | Colossal  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können die Pfeilspitzengröße auch im Dialogfeld **Linie** festlegen. 
  
Um einen Verweis auf die Zelle BeginArrowSize anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | BeginArrowSize  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die BeginArrowSize-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLine** <br/> |
| Zellenindex:  <br/> |**visLineBeginArrowSize** <br/> |
   

