---
title: Zelle XRulerDensity Cell (Ruler &amp; Grid section)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331850"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a>Zelle XRulerDensity Cell (Ruler &amp; Grid section)

Legt die horizontalen Einteilungen auf dem Lineal des Zeichenblatts fest.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Fest  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |Grob  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |Normal (Standard)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Abgestimmter  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Zelle entspricht der Option horizontale unter **Einheiten** im Dialogfeld **** **Lineal &amp; -Raster** (Klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil). 
  
Wenn Sie einen Verweis auf die Zelle Zelle XRulerDensity aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle XRulerDensity  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle XRulerDensity aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowRulerGrid** <br/> |
|Zellenindex:  <br/> |**visXRulerDensity** <br/> |
   

