---
title: Zelle "ShdwOffsetY" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm930
localization_priority: Normal
ms.assetid: f3f53a7d-7450-b2b0-b508-6044a87450d9
description: Legt den Abstand in Seiteneinheiten fest, den der Schlagschatten eines Shapes auf vertikaler Ebene vom Shape entfernt ist.
ms.openlocfilehash: 0228fef00230dd1517d20067fda855225cef5533
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798096"
---
# <a name="shdwoffsety-cell-page-properties-section"></a>Zelle "ShdwOffsetY" (Abschnitt "Page Properties")

Legt den Abstand in Seiteneinheiten fest, den der Schlagschatten eines Shapes auf vertikaler Ebene vom Shape entfernt ist.
  
## <a name="remarks"></a>Bemerkungen

Dieser Wert wird im Dialogfeld **Seite einrichten** festgelegt (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten** ). Dieser Wert ist unabhängig von der Skalierung der Zeichnung. Wenn die Zeichnung skaliert wird, bleibt der Offset des Schattens gleich. 
  
Wenn Sie einen Verweis auf die Zelle ShdwOffsetY nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShdwOffsetY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ShdwOffsetY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageShdwOffsetY** <br/> |
   

