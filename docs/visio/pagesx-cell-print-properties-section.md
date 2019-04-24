---
title: Zelle "PagesX" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60064
localization_priority: Normal
ms.assetid: a10bf4c2-24f4-4c53-39ba-2b8cd5b50d2c
description: Bestimmt die Anzahl der Druckseiten, auf denen das Zeichenblatt horizontal dargestellt werden soll.
ms.openlocfilehash: e912aef2277f5a7d2af5352897654ee986836c48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340138"
---
# <a name="pagesx-cell-print-properties-section"></a>Zelle "PagesX" (Abschnitt "Print Properties")

Bestimmt die Anzahl der Druckseiten, auf denen das Zeichenblatt horizontal dargestellt werden soll. 
  
## <a name="remarks"></a>Bemerkungen

Dieser Wert wird nur dann verwendet, wenn die Zelle OnPage auf WAHR festgelegt ist. 
  
Wenn Sie einen Verweis auf die Zelle PagesX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PagesX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PagesX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
| Zeilenindex:  <br/> |**visPrintPropertiesPagesX** <br/> |
   

