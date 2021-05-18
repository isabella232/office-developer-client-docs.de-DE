---
title: Zelle "YRulerDensity" (Abschnitt "Ruler &amp; Grid")
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
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a>Zelle "YRulerDensity" (Abschnitt "Ruler &amp; Grid")

Legt die vertikalen Einteilungen auf dem Lineal des Zeichenblatts fest.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Fest  <br/> |**visRulerFixed** <br/> |
|8 ( &amp; H8)  <br/> |Vorschrr  <br/> |**visRulerCoarse** <br/> |
|16 ( &amp; H10)  <br/> |Normal (Standard)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Fine  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Zelle entspricht der vertikalen **Unterteilungsoption** im Dialogfeld  Linealraster (klicken Sie auf der Registerkarte Ansicht auf den **Pfeil anzeigen).** **&amp;** 
  
Um einen Verweis auf die Zelle YRulerDensity anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |YRulerDensity  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle YRulerDensity nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowRulerGrid** <br/> |
|Zellenindex:  <br/> |**visYRulerDensity** <br/> |
   

