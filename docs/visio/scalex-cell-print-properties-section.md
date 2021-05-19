---
title: Zelle "ScaleX" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
localization_priority: Normal
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf der Druckerseite an.
ms.openlocfilehash: d1c2f6c184f987e1e7190b1c208310b83a823ee3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410210"
---
# <a name="scalex-cell-print-properties-section"></a>Zelle "ScaleX" (Abschnitt "Print Properties")

Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf der Druckerseite an.
  
## <a name="remarks"></a>Hinweise

Dieser Wert wird nur verwendet, wenn der OnPage-Zellwert FALSE ist. Die Zellen ScaleX und ScaleY haben immer denselben Wert, der dem  Wert in  der Einstellung Anpassen an  auf der Registerkarte Setup drucken im Dialogfeld Seiteneinrichtung entspricht (klicken Sie auf der Registerkarte Entwurf auf den Pfeil Seite **einrichten).**  
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle ScaleX anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ScaleX  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ScaleX-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesScaleX** <br/> |
   

