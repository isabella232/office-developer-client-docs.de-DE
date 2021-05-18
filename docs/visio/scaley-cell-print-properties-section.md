---
title: Zelle "ScaleY" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
localization_priority: Normal
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf der Druckerseite an.
ms.openlocfilehash: 0f8e86675a039002b60438eac7df92f4a2b13b98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406990"
---
# <a name="scaley-cell-print-properties-section"></a>Zelle "ScaleY" (Abschnitt "Print Properties")

Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf der Druckerseite an.
  
## <a name="remarks"></a>Hinweise

Dieser Wert wird nur verwendet, wenn der OnPage-Zellwert FALSE ist. Die Zellen ScaleX und ScaleY haben immer denselben Wert, der dem  Wert in  der Einstellung Anpassen an  auf der Registerkarte Setup drucken im Dialogfeld Seiteneinrichtung entspricht (klicken Sie auf der Registerkarte Entwurf auf den Pfeil Seite **einrichten).**  
  
Um einen Verweis auf die Zelle ScaleY anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ScaleY  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ScaleY nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesScaleY** <br/> |
   

