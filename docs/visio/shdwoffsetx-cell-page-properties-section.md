---
title: Zelle "ShdwOffsetX" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
localization_priority: Normal
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: Legt den Abstand in Seiteneinheiten fest, den der Schlagschatten eines Shapes auf horizontaler Ebene vom Shape entfernt ist.
ms.openlocfilehash: 9aec108146e329d7a8161acc4ca7cdcb19424eff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798079"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a>ShdwOffsetX Cell (Page Properties Section)

Legt den Abstand in Seiteneinheiten fest, den der Schlagschatten eines Shapes auf horizontaler Ebene vom Shape entfernt ist.
  
## <a name="remarks"></a>Bemerkungen

Dieser Wert wird im Dialogfeld **Seite einrichten** festgelegt (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten** ). Dieser Wert ist unabhängig von der Skalierung der Zeichnung. Wenn die Zeichnung skaliert wird, bleibt der Offset des Schattens gleich. 
  
Wenn Sie einen Verweis auf die Zelle ShdwOffsetX nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShdwOffsetX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ShdwOffsetX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageShdwOffsetX** <br/> |
   

