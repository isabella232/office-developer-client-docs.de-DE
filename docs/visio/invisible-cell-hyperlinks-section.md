---
title: Zelle "Invisible" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033755
localization_priority: Normal
ms.assetid: e67dcd83-4a88-a0f8-5c6a-dae51424edbd
description: Gibt an, ob im Kontextmenü eines Shapes oder einer Seite ein Hyperlink angezeigt wird.
ms.openlocfilehash: b52da8244bf31e75bacbb6f24f73eba6ee8c6e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404631"
---
# <a name="invisible-cell-hyperlinks-section"></a>Zelle "Invisible" (Abschnitt "Hyperlinks")

Gibt an, ob im Kontextmenü eines Shapes oder einer Seite ein Hyperlink angezeigt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Im Kontextmenü wird kein Hyperlink als Menüelement angezeigt.  <br/> |
|FALSE  <br/> |Im Kontextmenü wird ein Hyperlink als Menüelement angezeigt (Standardwert).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle inVisible aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Hyperlink. *Name* . Unsichtbar, wobei Hyperlink *. Name* der Zeilenname ist  <br/> |
   
Wenn Sie einen Verweis auf die unsichtbare Zelle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
|Zeilenindex:  <br/> |**visRow1stHyperlink** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visHLinkInvisible** <br/> |
   

