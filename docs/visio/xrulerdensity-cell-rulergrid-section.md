---
title: Zelle "XRulerDensity" (Abschnitt "Ruler &amp; Grid")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Legt die horizontalen Einteilungen auf dem Lineal des Zeichenblatts fest.
ms.openlocfilehash: f459e5d1d19580201f1404ac2d1ae53c824293f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411470"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a>Zelle "XRulerDensity" (Abschnitt "Ruler &amp; Grid")

Legt die horizontalen Einteilungen auf dem Lineal des Zeichenblatts fest.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Fest  <br/> |**visRulerFixed** <br/> |
|8 ( &amp; H8)  <br/> |Vorschrr  <br/> |**visRulerCoarse** <br/> |
|16 ( &amp; H10)  <br/> |Normal (Standard)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Fine  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Zelle entspricht der horizontalen **Unterteilungsoption** im Dialogfeld  Linealraster (klicken Sie auf der Registerkarte Ansicht auf den **Pfeil anzeigen).** **&amp;** 
  
Um einen Verweis auf die Zelle XRulerDensity anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |XRulerDensity  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die XRulerDensity-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowRulerGrid** <br/> |
|Zellenindex:  <br/> |**visXRulerDensity** <br/> |
   

