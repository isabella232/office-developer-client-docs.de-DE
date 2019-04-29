---
title: Zelle "ShdwObliqueAngle" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
localization_priority: Normal
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: Enthält eine Zahl, die den Winkel der Schräge angibt, wenn Sie den Standardzeichenblatt-Schattentyp anwenden.
ms.openlocfilehash: 2eca29bbc735c7101ca82a2f26db30b2e344b8e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430427"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a>Zelle "ShdwObliqueAngle" (Abschnitt "Page Properties")

Enthält eine Zahl, die den Winkel der Schräge angibt, wenn Sie den Standardzeichenblatt-Schattentyp anwenden.
  
## <a name="remarks"></a>Bemerkungen

Der Wert Null (0) in dieser Zelle zeigt an, dass die Winkelrichtung genau nach oben verläuft und im Uhrzeigersinn gemessen wird.
  
 Der in dieser Zelle beschriebene Winkel wird verwendet, wenn die Zelle-Zelle (der Schattentyp für ein Shape auf dem Zeichenblatt) auf Seiten Standard (**visFSTPageDefault** ) festgelegt ist und der Schattentyp schräg ist. Der standardmäßige Seiten Schattentyp wird in der Zelle "ShdwType definiert. 
  
Wenn Sie dieses Verhalten für einen einzelnen Schatten festlegen möchten, verwenden Sie im Abschnitt Fill Format die Zelle ShapeShdwObliqueAngle.
  
Wenn Sie einen Verweis auf die Zelle "ShdwObliqueAngle aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | "ShdwObliqueAngle  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "ShdwObliqueAngle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageShdwObliqueAngle** <br/> |
   

