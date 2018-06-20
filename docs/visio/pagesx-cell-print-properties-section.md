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
ms.openlocfilehash: 4f1cf3286e7b54dc90925bf2f1ab9fe8532022e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797596"
---
# <a name="pagesx-cell-print-properties-section"></a>PagesX Cell (Print Properties Section)

Bestimmt die Anzahl der Druckseiten, auf denen das Zeichenblatt horizontal dargestellt werden soll. 
  
## <a name="remarks"></a>Hinweise

Dieser Wert wird nur dann verwendet, wenn die Zelle OnPage auf WAHR festgelegt ist. 
  
Wenn Sie einen Verweis auf die Zelle PagesX nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PagesX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PagesX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
| Zellenindex:  <br/> |**visPrintPropertiesPagesX** <br/> |
   

