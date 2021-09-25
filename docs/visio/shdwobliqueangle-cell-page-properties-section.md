---
title: Zelle "ShdwObliqueAngle" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
ms.localizationpriority: medium
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: Enthält eine Zahl, die den Winkel der Schräge angibt, wenn Sie den Standardzeichenblatt-Schattentyp anwenden.
ms.openlocfilehash: 4982d531663eaf7a854e1a50a50e57b8c52086f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570064"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a>Zelle "ShdwObliqueAngle" (Abschnitt "Page Properties")

Enthält eine Zahl, die den Winkel der Schräge angibt, wenn Sie den Standardzeichenblatt-Schattentyp anwenden.
  
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert Null (0) in dieser Zelle zeigt an, dass die Winkelrichtung genau nach oben verläuft und im Uhrzeigersinn gemessen wird.
  
 Der in dieser Zelle beschriebene Winkel wird immer dann verwendet, wenn die ShapeShdwType Cell (der Schattentyp für ein Shape auf der Seite) auf Page Default (**visFSTPageDefault** ) festgelegt ist und der Schattentyp schräg ist. Der Standardmäßige Seitenschattentyp wird in der Zelle ShdwType definiert. 
  
Wenn Sie dieses Verhalten für einen einzelnen Schatten festlegen möchten, verwenden Sie im Abschnitt Fill Format die Zelle ShapeShdwObliqueAngle.
  
Um einen Verweis auf die Zelle "ShdwObliqueAngle" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShdwObliqueAngle  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShdwObliqueAngle anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageShdwObliqueAngle** <br/> |
   

