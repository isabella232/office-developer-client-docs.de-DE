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
ms.openlocfilehash: e269c5e907afa0d49f1fc6115b7a031835467c2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797225"
---
# <a name="invisible-cell-hyperlinks-section"></a>Invisible Cell (Hyperlinks Section)

Gibt an, ob im Kontextmenü eines Shapes oder einer Seite ein Hyperlink angezeigt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|WAHR  <br/> |Im Kontextmenü wird kein Hyperlink als Menüelement angezeigt.  <br/> |
|FALSCH  <br/> |Im Kontextmenü wird ein Hyperlink als Menüelement angezeigt (Standardwert).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Invisible aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Hyperlink. *Name* . Unsichtbar, in dem Hyperlink *.name* der Zeilenname ist  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Invisible aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
|Zeilenindex:  <br/> |**visRow1stHyperlink** +  *i* wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visHLinkInvisible** <br/> |
   

