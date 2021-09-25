---
title: Zelle "YGridDensity" (Abschnitt "Ruler &amp; Grid")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
ms.localizationpriority: medium
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Gibt den Typ des zu verwendenden vertikalen Gitters an.
ms.openlocfilehash: 71b592831e6b84ea8ac7ad142ae5ad1b4c475a0e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553536"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a>Zelle "YGridDensity" (Abschnitt "Ruler &amp; Grid")

Gibt den Typ des zu verwendenden vertikalen Gitters an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Fest  <br/> |**visGridFixed** <br/> |
|2  <br/> |Grob  <br/> |**visGridCoarse** <br/> |
|4   <br/> |Normal (Standard)  <br/> |**visGridNormal** <br/> |
|8   <br/> |Fein  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Zelle entspricht der vertikalen Option für den **Rasterabstand** im Dialogfeld **&amp; Linealraster** (klicken Sie auf **der** Registerkarte Ansicht auf den Pfeil **anzeigen).** 
  
Um einen Verweis auf die Zelle "YGridDensity" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |YGridDensity  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle YGridDensity anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowRulerGrid** <br/> |
|Zellenindex:  <br/> |**visYGridDensity** <br/> |
   

