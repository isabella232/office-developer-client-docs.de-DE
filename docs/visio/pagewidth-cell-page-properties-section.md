---
title: Zelle "PageWidth" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251372
localization_priority: Normal
ms.assetid: b98c5bf3-10c8-7299-2836-3906d6a9135d
description: Legt die Breite der gedruckten Seite in Zeichnungseinheiten fest.
ms.openlocfilehash: 6d887cb4335d2725101db54ba2b1483ccf01cff4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434270"
---
# <a name="pagewidth-cell-page-properties-section"></a>Zelle "PageWidth" (Abschnitt "Page Properties")

Legt die Breite der gedruckten Seite in Zeichnungseinheiten fest.
  
## <a name="remarks"></a>Hinweise

Sie können die Seitenbreite  auch auf der  Registerkarte Seitengröße des Dialogfelds Seiteneinrichtung festlegen (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil Seite **einrichten)** oder indem Sie die Größe der Seite mit der Maus manuell ändern. Ziehen Sie dazu bei gedrückter STRG-TASTE den Seitenrand mit der Maus. 
  
Um einen Verweis auf die Zelle PageWidth anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PageWidth  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die PageWidth-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageWidth** <br/> |
   

