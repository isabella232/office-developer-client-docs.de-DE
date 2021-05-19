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
ms.openlocfilehash: 0f9d1e4b1294dea3f211c8d0d69ffc49b6180066
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342231"
---
# <a name="newwindow-cell-hyperlinks-section"></a>Zelle "NewWindow" (Abschnitt "Hyperlinks")

Gibt an, ob der Hyperlink in einem neuen Fenster geöffnet werden soll.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Öffnen Sie die verknüpfte Seite, das Dokument oder die Website in einem neuen Fenster.  <br/> |
| FALSE  <br/> | Standard. Hyperlink nicht in einem neuen Fenster öffnen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle NewWindow anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Hyperlink.  *Name*  . NewWindow, wobei Hyperlink.  *Name*  ist der Zeilenname  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die NewWindow-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
| Zeilenindex:  <br/> |**visRow1stHyperlink**  +   *i* where *i* = 0, 1, 2, ...  <br/> |
| Zellenindex:  <br/> |**visHLinkNewWin** <br/> |
   

