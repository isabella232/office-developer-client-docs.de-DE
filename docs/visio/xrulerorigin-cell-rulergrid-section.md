---
title: Zelle "XRulerOrigin" (Lineal &amp; Rasterabschnitt)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1170
localization_priority: Normal
ms.assetid: 328f8ab5-217f-0336-0d56-611eff509fe8
description: Gibt den Nullpunkt auf der x-Achse-Achsenlineal des Zeichenblatts an.
ms.openlocfilehash: 78fab70c8489ddcdfe450ef9f9fd88b6c5040211
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798446"
---
# <a name="xrulerorigin-cell-ruler-amp-grid-section"></a>Zelle "XRulerOrigin" (Lineal &amp; Rasterabschnitt)

Gibt den Nullpunkt auf der x-Achse-Achsenlineal des Zeichenblatts an.
  
## <a name="remarks"></a>Hinweise

Diese Zelle entspricht der horizontalen Option **Linealursprung** in die **Lineal &amp; Raster** im Dialogfeld (klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil neben **Anzeigen** ). 
  
Wenn Sie einen Verweis auf die Zelle XRulerOrigin nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |XRulerOrigin  <br/> |
   
Wenn Sie einen Verweis auf die Zelle XRulerOrigin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowRulerGrid** <br/> |
|Zellenindex:  <br/> |**visXRulerOrigin** <br/> |
   

