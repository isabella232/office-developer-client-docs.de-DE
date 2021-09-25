---
title: Zelle "PageBottomMargin" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60060
ms.localizationpriority: medium
ms.assetid: 7a97e97c-278d-2e1e-6c4f-f5f32e2cdeb0
description: Gibt den unteren Rand der gedruckten Seite an.
ms.openlocfilehash: 32e411b476bdd943e2294b7ba9943653ff0ce41c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577801"
---
# <a name="pagebottommargin-cell-print-properties-section"></a>Zelle "PageBottomMargin" (Abschnitt "Print Properties")

Gibt den unteren Rand der gedruckten Seite an.
  
## <a name="remarks"></a>HinwBemerkungeneise

Durch diesen Wert werden physische Einheiten dargestellt, und er wird weder durch Skalierung noch durch Zeichnungseinheiten beeinflusst. Wenn diese Zelle beispielsweise den Wert 0,5 cm aufweist, beträgt der Rand 0,5 Zentimeter, selbst wenn als Einheit der Seite Dezimeter angegeben werden. Wenn keine Einheiten explizit angegeben sind, ist die Standardeinstellung Seiteneinheiten. 
  
Um einen Verweis auf die Zelle "PageBottomMargin" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PageBottomMargin  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PageBottomMargin anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
| Zeilenindex:  <br/> |**visPrintPropertiesBottomMargin** <br/> |
   

