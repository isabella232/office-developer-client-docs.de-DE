---
title: Zelle "XGridDensity" (Lineal &amp; Rasterabschnitt)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Gibt den Typ des zu verwendenden horizontalen Gitters an.
ms.openlocfilehash: 107cde8e8b0d630a4dc4b43127412de2f6b0115d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798440"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>Zelle "XGridDensity" (Lineal &amp; Rasterabschnitt)

Gibt den Typ des zu verwendenden horizontalen Gitters an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Fest  <br/> |**visGridFixed** <br/> |
|2  <br/> |Grob  <br/> |**visGridCoarse** <br/> |
|4  <br/> |Normal (Standard)  <br/> |**visGridNormal** <br/> |
|8  <br/> |Fein  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Zelle entspricht der horizontalen **Gitterabstand** option in der **Lineal &amp; Raster** im Dialogfeld (klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil neben **Anzeigen** ). 
  
Wenn Sie einen Verweis auf die Zelle XGridDensity nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |XGridDensity  <br/> |
   
Wenn Sie einen Verweis auf die Zelle XGridDensity aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowRulerGrid** <br/> |
|Zellenindex:  <br/> |**visXGridDensity** <br/> |
   

