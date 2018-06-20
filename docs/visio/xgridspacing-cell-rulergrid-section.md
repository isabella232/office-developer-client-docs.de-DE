---
title: Zelle "XGridSpacing" (Lineal &amp; Rasterabschnitt)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
localization_priority: Normal
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: Gibt den Abstand zwischen den horizontalen Linien eines festen Gitters an (XGridDensity = 0).
ms.openlocfilehash: 5f461d02dae1574fe2b186b43166ef14d8251df2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798434"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a>Zelle "XGridSpacing" (Lineal &amp; Rasterabschnitt)

Gibt den Abstand zwischen den horizontalen Linien eines festen Gitters an (XGridDensity = 0).
  
## <a name="remarks"></a>Bemerkungen

Diese Zelle entspricht der horizontalen **minimaler Abstand** option in der **Lineal &amp; Raster** im Dialogfeld (klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil neben **Anzeigen** ). 
  
Wenn Sie einen Verweis auf die Zelle XGridSpacing nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |XGridSpacing  <br/> |
   
Wenn Sie einen Verweis auf die Zelle XGridSpacing aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowRulerGrid** <br/> |
|Zellenindex:  <br/> |**visXGridSpacing** <br/> |
   

