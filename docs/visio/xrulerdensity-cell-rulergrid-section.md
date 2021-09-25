---
title: Zelle "XRulerDensity" (Abschnitt "Ruler &amp; Grid")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
ms.localizationpriority: medium
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Legt die horizontalen Einteilungen auf dem Lineal des Zeichenblatts fest.
ms.openlocfilehash: 23eacc8e1a99df92bf9cdb705adda6cb3ecad890
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603109"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a>Zelle "XRulerDensity" (Abschnitt "Ruler &amp; Grid")

Legt die horizontalen Einteilungen auf dem Lineal des Zeichenblatts fest.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Fest  <br/> |**visRulerFixed** <br/> |
|8 ( &amp; H8)  <br/> |Grob  <br/> |**visRulerCoarse** <br/> |
|16 ( &amp; H10)  <br/> |Normal (Standard)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Fein  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Zelle entspricht der Horizontalen **Unterteilungsoption** im Dialogfeld **&amp; Linealraster** (klicken Sie auf **der** Registerkarte Ansicht auf den Pfeil **anzeigen).** 
  
Um einen Verweis auf die Zelle "XRulerDensity" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |XRulerDensity  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle XRulerDensity anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowRulerGrid** <br/> |
|Zellenindex:  <br/> |**visXRulerDensity** <br/> |
   

