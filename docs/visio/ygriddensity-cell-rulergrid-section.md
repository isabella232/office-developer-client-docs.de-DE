---
title: Zelle YGridDensity Cell (Ruler &amp; Grid section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Gibt den Typ des zu verwendenden vertikalen Gitters an.
ms.openlocfilehash: 793fa40316edd591c8b4873d8919507c2393b5d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429810"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a>Zelle YGridDensity Cell (Ruler &amp; Grid section)

Gibt den Typ des zu verwendenden vertikalen Gitters an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Fest  <br/> |**visGridFixed** <br/> |
|2  <br/> |Grob  <br/> |**visGridCoarse** <br/> |
|4  <br/> |Normal (Standard)  <br/> |**visGridNormal** <br/> |
|8  <br/> |Abgestimmter  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Zelle entspricht der Option vertikaler **Rasterabstand** im Dialogfeld **** ** &amp; Lineal (Raster** ) (Klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil). 
  
Wenn Sie einen Verweis auf die Zelle Zelle YGridDensity aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle YGridDensity  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle YGridDensity aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowRulerGrid** <br/> |
|Zellenindex:  <br/> |**visYGridDensity** <br/> |
   

