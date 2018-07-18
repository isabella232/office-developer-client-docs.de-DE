---
title: YRulerOrigin Cell (Ruler &amp; Grid Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1220
localization_priority: Normal
ms.assetid: 5d21b64f-a559-76ef-06df-d24c048cc6ef
description: Gibt den Nullpunkt auf dem Y-Achsenlineal des Zeichenblatts an.
ms.openlocfilehash: 143f372d66ee25e90608a9b2eb252a99e7bcc52f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798473"
---
# <a name="yrulerorigin-cell-ruler-amp-grid-section"></a>YRulerOrigin Cell (Ruler &amp; Grid Section)

Gibt den Nullpunkt auf dem Y-Achsenlineal des Zeichenblatts an.
  
## <a name="remarks"></a>Bemerkungen

Diese Zelle entspricht der vertikalen Option **Linealursprung** in die **Lineal &amp; Raster** im Dialogfeld (klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil neben **Anzeigen** ). 
  
Wenn Sie einen Verweis auf die Zelle YRulerOrigin aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |YRulerOrigin  <br/> |
   
Wenn Sie einen Verweis auf die Zelle YRulerOrigin aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowRulerGrid** <br/> |
|Zellenindex:  <br/> |**visYRulerOrigin** <br/> |
   

