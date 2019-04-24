---
title: Zelle "Frame" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm405
localization_priority: Normal
ms.assetid: f71d8737-92ef-1124-ba4a-b7e17305bd0a
description: Stellt den Namen eines Zielframes dar, wenn die Anwendung als aktives Dokument in einer Containeranwendung geöffnet ist. Der Standardwert ist eine leere Zeichenfolge.
ms.openlocfilehash: 8f41e5bf854e31e1f17eabb2aecbded55175ebaf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344852"
---
# <a name="frame-cell-hyperlinks-section"></a>Zelle "Frame" (Abschnitt "Hyperlinks")

Stellt den Namen eines Zielframes dar, wenn die Anwendung als aktives Dokument in einer Containeranwendung geöffnet ist. Der Standardwert ist eine leere Zeichenfolge.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle "Frame" aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Hyperlink.  *Name* . Frame, auf dem Hyperlink.  *Name* ist der Name der Zeile  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Rahmen aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
| Zeilenindex:  <br/> |**visRow1stHyperlink** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visHLinkFrame** <br/> |
   

