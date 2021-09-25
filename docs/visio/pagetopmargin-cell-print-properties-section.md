---
title: Zelle "PageTopMargin" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033785
ms.localizationpriority: medium
ms.assetid: 2ba0fd22-65a6-6cb6-da00-08f391705544
description: Gibt den oberen Rand der gedruckten Seite an.
ms.openlocfilehash: 6b91f219f28f148aa6e341668d0ba0bd25437272
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577773"
---
# <a name="pagetopmargin-cell-print-properties-section"></a>Zelle "PageTopMargin" (Abschnitt "Print Properties")

Gibt den oberen Rand der gedruckten Seite an.
  
## <a name="remarks"></a>HinwBemerkungeneise

Durch diesen Wert werden physische Einheiten dargestellt, und er wird weder durch Skalierung noch durch Zeichnungseinheiten beeinflusst. Wenn diese Zelle beispielsweise den Wert 0,25 cm aufweist, beträgt der Rand 0,25 Zentimeter, selbst wenn als Einheit der Seite Dezimeter angegeben werden. Wenn keine Einheiten explizit angegeben sind, ist die Standardeinstellung Seiteneinheiten. 
  
Um einen Verweis auf die Zelle "PageTopMargin" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PageTopMargin  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PageTopMargin anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
| Zeilenindex:  <br/> |**visPrintPropertiesTopMargin** <br/> |
   

