---
title: Zelle XRulerOrigin Cell (Ruler &amp; Grid section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1170
localization_priority: Normal
ms.assetid: 328f8ab5-217f-0336-0d56-611eff509fe8
description: Gibt den Nullpunkt auf dem X-Achsenlineal des Zeichenblatts an.
ms.openlocfilehash: d66fd324718ec46b1209c4726eeb2d27c21db8b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435327"
---
# <a name="xrulerorigin-cell-ruler-amp-grid-section"></a>Zelle XRulerOrigin Cell (Ruler &amp; Grid section)

Gibt den Nullpunkt auf dem X-Achsenlineal des Zeichenblatts an.
  
## <a name="remarks"></a>Bemerkungen

Diese Zelle entspricht der Option horizontales **Lineal** im Dialogfeld **Lineal &amp; -Raster** (Klicken Sie auf der Registerkarte **Ansicht** auf **** den Pfeil). 
  
Wenn Sie einen Verweis auf die Zelle Zelle XRulerOrigin aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle XRulerOrigin  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle XRulerOrigin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowRulerGrid** <br/> |
|Zellenindex:  <br/> |**visXRulerOrigin** <br/> |
   

