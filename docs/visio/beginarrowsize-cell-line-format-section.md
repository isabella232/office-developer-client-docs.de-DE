---
title: Zelle "BeginArrowSize" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251629
ms.localizationpriority: medium
ms.assetid: bfddb829-6e13-7d74-b9b9-2cb5c0937bae
description: Bestimmt die Pfeilspitzengröße am Linienanfang.
ms.openlocfilehash: ed1db98de60368f2c08d8c5e61c1185cce016be2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628843"
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
| 5  <br/> | Jumbo  <br/> |**visArrowSizeJumbo** <br/> |
| 6   <br/> | Kolossale  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können die Pfeilspitzengröße auch im Dialogfeld **Linie** festlegen. 
  
Verwenden Sie zum Abrufen eines Verweises auf die Zelle "BeginArrowSize" anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | BeginArrowSize  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle BeginArrowSize anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLine** <br/> |
| Zellenindex:  <br/> |**visLineBeginArrowSize** <br/> |
   

