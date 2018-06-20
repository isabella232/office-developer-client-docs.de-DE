---
title: Zelle "NewWindow" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
localization_priority: Normal
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: Gibt an, ob der Hyperlink in einem neuen Fenster geöffnet werden soll.
ms.openlocfilehash: b4d927e1970e994047df3cb89afa7799a825511d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797542"
---
# <a name="newwindow-cell-hyperlinks-section"></a>NewWindow Cell (Hyperlinks Section)

Gibt an, ob der Hyperlink in einem neuen Fenster geöffnet werden soll.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Verknüpfte Seite, Dokument oder Website in einem neuen Fenster öffnen.  <br/> |
| FALSE  <br/> | Standard. Hyperlink nicht in einem neuen Fenster öffnen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle NewWindow nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Hyperlink.  *Name* . NewWindow, in dem Hyperlink.  *Name* ist der Zeilenname  <br/> |
   
Wenn Sie einen Verweis auf die Zelle NewWindow aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
| Zeilenindex:  <br/> |**visRow1stHyperlink** +  *i* wobei *i* = 0, 1, 2,...  <br/> |
| Zellenindex:  <br/> |**visHLinkNewWin** <br/> |
   

