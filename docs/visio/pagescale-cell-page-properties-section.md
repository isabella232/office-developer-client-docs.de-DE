---
title: Zelle "PageScale" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm775
localization_priority: Normal
ms.assetid: e1da84b3-fd15-12b9-9342-0412e818b3b9
description: Bestimmt den Wert der Seiteneinheit im aktuellen Zeichnungsmaßstab. Der Zeichnungsmaßstab für die Seite ist das Verhältnis der in der Zelle PageScale angezeigten Seiteneinheit zur in der Zelle DrawingScale angezeigten Zeichnungseinheit.
ms.openlocfilehash: 0763fd6fad5f64bc741cbdd1e1227b0982323841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405534"
---
# <a name="pagescale-cell-page-properties-section"></a>Zelle "PageScale" (Abschnitt "Page Properties")

Bestimmt den Wert der Seiteneinheit im aktuellen Zeichnungsmaßstab. Der Zeichnungsmaßstab für die Seite ist das Verhältnis der in der Zelle PageScale angezeigten Seiteneinheit zur in der Zelle DrawingScale angezeigten Zeichnungseinheit.
  
## <a name="remarks"></a>Hinweise

Sie können den Wert der Zelle PageScale auch auf  der Registerkarte Zeichnungsskala im Dialogfeld Seiteneinrichtung festlegen (klicken Sie auf der Registerkarte Entwurf auf den **Pfeil Seite einrichten).**   Der Wert der Zelle ist die erste  der beiden Zahlen  im Feld Vordefinierte Skalierung oder benutzerdefinierte Skalierung, abhängig von der Zeichnungsskaleneinstellung, die unter **Zeichnungsskala ausgewählt ist.** Wenn Sie beispielsweise eine Architekturskala für Ihre Zeichnung auswählen, ist die Zeichnungsskala für die Seite 3/32" = 1'0". Der Wert in der Zelle PageScale ist 0,0938 in. (oder 3/32") und der Wert in der Zelle DrawingScale beträgt 1 ft.
  
Um einen Verweis auf die Zelle PageScale anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PageScale  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PageScale nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageScale** <br/> |
   

