---
title: Zelle "ScaleX" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
ms.localizationpriority: medium
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf dem Druckerblatt an.
ms.openlocfilehash: 457aec2fdb00c082e9689f9b0a98e5104af39893
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573432"
---
# <a name="scalex-cell-print-properties-section"></a>Zelle "ScaleX" (Abschnitt "Print Properties")

Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf dem Druckerblatt an.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieser Wert wird nur verwendet, wenn der OnPage-Zellwert FALSE ist. Die Zellen "ScaleX" und "ScaleY" haben immer denselben Wert, der dem Wert in der Einstellung **"Anpassen an"** auf der Registerkarte **"Druckeinrichtung"** im Dialogfeld **"Seite einrichten"** entspricht (klicken Sie auf der Registerkarte **"Entwurf"** auf den Pfeil neben **"Seite einrichten").** 
  
Um einen Verweis auf die Zelle ScaleX anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Scalex  <br/> |
   
Um einen Verweis auf die Zelle ScaleX anhand des Indexes aus einem Programm abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesScaleX** <br/> |
   

