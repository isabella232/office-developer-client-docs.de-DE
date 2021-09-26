---
title: Zelle "XGridDensity" (Abschnitt "Ruler &amp; Grid")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
ms.localizationpriority: medium
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Gibt den Typ des zu verwendenden horizontalen Gitters an.
ms.openlocfilehash: ef2e65acde1121c1c4e822697867bf5a17d9102f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597716"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>Zelle "XGridDensity" (Abschnitt "Ruler &amp; Grid")

Gibt den Typ des zu verwendenden horizontalen Gitters an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Fest  <br/> |**visGridFixed** <br/> |
|2  <br/> |Grob  <br/> |**visGridCoarse** <br/> |
|4   <br/> |Normal (Standard)  <br/> |**visGridNormal** <br/> |
|8   <br/> |Fein  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Zelle entspricht der horizontalen Option für den **Rasterabstand** im Dialogfeld **&amp; Linealraster** (klicken Sie auf **der** Registerkarte Ansicht auf den Pfeil **anzeigen).** 
  
Um einen Verweis auf die Zelle "XGridDensity" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |XGridDensity  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle XGridDensity anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowRulerGrid** <br/> |
|Zellenindex:  <br/> |**visXGridDensity** <br/> |
   

