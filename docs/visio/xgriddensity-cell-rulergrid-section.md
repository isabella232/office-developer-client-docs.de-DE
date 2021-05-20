---
title: Zelle "XGridDensity" (Abschnitt "Ruler &amp; Grid")
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
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>Zelle "XGridDensity" (Abschnitt "Ruler &amp; Grid")

Gibt den Typ des zu verwendenden horizontalen Gitters an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Fest  <br/> |**visGridFixed** <br/> |
|2  <br/> |Vorschrr  <br/> |**visGridCoarse** <br/> |
|4   <br/> |Normal (Standard)  <br/> |**visGridNormal** <br/> |
|8   <br/> |Fine  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Zelle entspricht der **Horizontalrasterabstandsoption** im Dialogfeld  **&amp; Linealraster** (klicken Sie auf der Registerkarte Ansicht auf den **Pfeil anzeigen).** 
  
Um einen Verweis auf die Zelle XGridDensity anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |XGridDensity  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die XGridDensity-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowRulerGrid** <br/> |
|Zellenindex:  <br/> |**visXGridDensity** <br/> |
   

