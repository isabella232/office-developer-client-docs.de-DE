---
title: Zelle XGridDensity Cell (Ruler &amp; Grid section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Gibt den Typ des zu verwendenden horizontalen Gitters an.
ms.openlocfilehash: 5ebd172e56a66bfb39bd9bfa20967bb6b52c5aa2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436041"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>Zelle XGridDensity Cell (Ruler &amp; Grid section)

Gibt den Typ des zu verwendenden horizontalen Gitters an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Fest  <br/> |**visGridFixed** <br/> |
|2  <br/> |Grob  <br/> |**visGridCoarse** <br/> |
|4  <br/> |Normal (Standard)  <br/> |**visGridNormal** <br/> |
|8  <br/> |Abgestimmter  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Zelle entspricht der horizontalen **Rasterabstand** Option im Dialogfeld **Lineal &amp; -Raster** (Klicken Sie auf der Registerkarte **Ansicht** auf **** den Pfeil). 
  
Wenn Sie einen Verweis auf die Zelle Zelle XGridDensity aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle XGridDensity  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle XGridDensity aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowRulerGrid** <br/> |
|Zellenindex:  <br/> |**visXGridDensity** <br/> |
   

