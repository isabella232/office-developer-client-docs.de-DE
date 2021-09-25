---
title: Zelle "NewWindow" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
ms.localizationpriority: medium
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: Gibt an, ob der Hyperlink in einem neuen Fenster geöffnet werden soll.
ms.openlocfilehash: b77da67f595ff25e235c2b2b01f292fe5b31013e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563000"
---
# <a name="newwindow-cell-hyperlinks-section"></a>Zelle "NewWindow" (Abschnitt "Hyperlinks")

Gibt an, ob der Hyperlink in einem neuen Fenster geöffnet werden soll.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Öffnen Sie die verknüpfte Seite, das Dokument oder die verknüpfte Website in einem neuen Fenster.  <br/> |
| FALSE  <br/> | Standard. Hyperlink nicht in einem neuen Fenster öffnen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle "NewWindow" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Hyperlink.  *Name*  . NewWindow where Hyperlink.  *Name*  ist der Zeilenname  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle NewWindow anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
| Zeilenindex:  <br/> |**visRow1stHyperlink**  +   *i* where *i* = 0, 1, 2, ...  <br/> |
| Zellenindex:  <br/> |**visHLinkNewWin** <br/> |
   

