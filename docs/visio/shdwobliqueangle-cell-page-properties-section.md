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
ms.openlocfilehash: 4549ce7b5202b4649a925b04ea54c0d5df569599
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798097"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a>ShdwObliqueAngle Cell (Page Properties Section)

Enthält eine Zahl, die den Winkel der Schräge angibt, wenn Sie den Standardzeichenblatt-Schattentyp anwenden.
  
## <a name="remarks"></a>Hinweise

Der Wert Null (0) in dieser Zelle zeigt an, dass die Winkelrichtung genau nach oben verläuft, sie wird im Uhrzeigersinn gemessen.
  
 Der Winkel in dieser Zelle beschriebene wird verwendet, wenn die Zelle ShapeShdwType (der Schattentyp für ein Shape auf dem Zeichenblatt) auf Seitenstandard (**VisFSTPageDefault** ) festgelegt ist, und der Schattentyp oblique ist. Der Standardzeichenblatt-Schattentyp wird in der Zelle ShdwType definiert. 
  
Wenn Sie dieses Verhalten für einen einzelnen Schatten festlegen möchten, verwenden Sie im Abschnitt Fill Format die Zelle ShapeShdwObliqueAngle.
  
Wenn Sie einen Verweis auf die Zelle ShdwObliqueAngle nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShdwObliqueAngle  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ShdwObliqueAngle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageShdwObliqueAngle** <br/> |
   

