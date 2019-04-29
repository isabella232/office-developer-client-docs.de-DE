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
ms.openlocfilehash: be7ec4cccd53cc9d74811e2e45122c8bc29497d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438141"
---
# <a name="shdwoffsety-cell-page-properties-section"></a>Zelle "ShdwOffsetY" (Abschnitt "Page Properties")

Legt den Abstand in Seiteneinheiten fest, den der Schlagschatten eines Shapes auf vertikaler Ebene vom Shape entfernt ist.
  
## <a name="remarks"></a>Bemerkungen

Dieser Wert wird im Dialogfeld **Seite einrichten** festgelegt (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Bei Größenänderung der Zeichnung bleibt der Schattenabstand gleich. 
  
Wenn Sie einen Verweis auf die Zelle "ShdwOffsetY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | "ShdwOffsetY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "ShdwOffsetY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageShdwOffsetY** <br/> |
   

