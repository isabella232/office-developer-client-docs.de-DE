---
title: Zelle "YGridDensity" (Lineal &amp; Rasterabschnitt)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Gibt den Typ des zu verwendenden vertikalen Gitters an.
ms.openlocfilehash: 4e0d1b1dc6f3da95b9328342e0398313b6c85eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798470"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a>Zelle "YGridDensity" (Lineal &amp; Rasterabschnitt)

Gibt den Typ des zu verwendenden vertikalen Gitters an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Fest  <br/> |**visGridFixed** <br/> |
|2  <br/> |Grob  <br/> |**visGridCoarse** <br/> |
|4  <br/> |Normal (Standard)  <br/> |**visGridNormal** <br/> |
|8  <br/> |Fein  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Zelle entspricht der vertikalen **Gitterabstand** option in der **Lineal &amp; Raster** im Dialogfeld (klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil neben **Anzeigen** ). 
  
Wenn Sie einen Verweis auf die Zelle YGridDensity nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |YGridDensity  <br/> |
   
Wenn Sie einen Verweis auf die Zelle YGridDensity aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowRulerGrid** <br/> |
|Zellenindex:  <br/> |**visYGridDensity** <br/> |
   

