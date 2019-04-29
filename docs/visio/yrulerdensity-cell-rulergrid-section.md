---
title: Zelle YRulerDensity Cell (Ruler &amp; Grid section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Legt die vertikalen Einteilungen auf dem Lineal des Zeichenblatts fest.
ms.openlocfilehash: c92c48f6c86fc794cf6f53a87fdb99e67a73b9f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406801"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a>Zelle YRulerDensity Cell (Ruler &amp; Grid section)

Legt die vertikalen Einteilungen auf dem Lineal des Zeichenblatts fest.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Fest  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |Grob  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |Normal (Standard)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Abgestimmter  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Zelle entspricht der Option vertikale unter **Einheiten** im Dialogfeld **** **Lineal &amp; -Raster** (Klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil). 
  
Wenn Sie einen Verweis auf die Zelle Zelle YRulerDensity aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle YRulerDensity  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle YRulerDensity aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowRulerGrid** <br/> |
|Zellenindex:  <br/> |**visYRulerDensity** <br/> |
   

