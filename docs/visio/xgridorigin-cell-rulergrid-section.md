---
title: Zelle "XGridOrigin" (Lineal &amp; Rasterabschnitt)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1155
localization_priority: Normal
ms.assetid: 2b1a8902-b1d4-c3d9-8c9f-1a28fddacc59
description: Gibt die horizontale Koordinate des Gitterursprungs an.
ms.openlocfilehash: 0cc6ff10f9bb4ba7ee0a13a48cb55b7dcd0fa013
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798445"
---
# <a name="xgridorigin-cell-ruler-amp-grid-section"></a>Zelle "XGridOrigin" (Lineal &amp; Rasterabschnitt)

Gibt die horizontale Koordinate des Gitterursprungs an.
  
## <a name="remarks"></a>Bemerkungen

Diese Zelle entspricht der horizontalen **Gitterursprung** option in der **Lineal &amp; Raster** im Dialogfeld (klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil **angezeigt** . 
  
Wenn Sie einen Verweis auf die Zelle XGridOrigin nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |XGridOrigin  <br/> |
   
Wenn Sie einen Verweis auf die Zelle XGridOrigin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowRulerGrid** <br/> |
|Zellenindex:  <br/> |**visXGridOrigin** <br/> |
   

