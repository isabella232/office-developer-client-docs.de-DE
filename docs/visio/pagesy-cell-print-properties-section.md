---
title: Zelle "PagesY" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033790
ms.localizationpriority: medium
ms.assetid: 396a0f3e-dbbb-3f5b-3c5d-f7dd454a765f
description: Bestimmt die Anzahl der Druckseiten, auf denen das Zeichenblatt vertikal dargestellt werden soll.
ms.openlocfilehash: 190cd49ff521a11c3daa70981bb17794a9a7b10b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627772"
---
# <a name="pagesy-cell-print-properties-section"></a>Zelle "PagesY" (Abschnitt "Print Properties")

Bestimmt die Anzahl der Druckseiten, auf denen das Zeichenblatt vertikal dargestellt werden soll. 
  
## <a name="remarks"></a>Bemerkungen

Dieser Wert wird nur dann verwendet, wenn die Zelle OnPage auf WAHR festgelegt ist. 
  
Um einen Verweis auf die Zelle PagesY anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PagesY  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PagesY anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
| Zeilenindex:  <br/> |**visPrintPropertiesPagesY** <br/> |
   

