---
title: Zelle "ScaleY" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
ms.localizationpriority: medium
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf dem Druckerblatt an.
ms.openlocfilehash: d4a84ef5a7d9d158ec64bab61cc18ffa6c794b97
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573425"
---
# <a name="scaley-cell-print-properties-section"></a>Zelle "ScaleY" (Abschnitt "Print Properties")

Gibt den Prozentsatz der Vergrößerung des Zeichenblatts auf dem Druckerblatt an.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieser Wert wird nur verwendet, wenn der OnPage-Zellwert FALSE ist. Die Zellen "ScaleX" und "ScaleY" haben immer denselben Wert, der dem Wert in der Einstellung **"Anpassen an"** auf der Registerkarte **"Druckeinrichtung"** im Dialogfeld **"Seite einrichten"** entspricht (klicken Sie auf der Registerkarte **"Entwurf"** auf den Pfeil neben **"Seite einrichten").** 
  
Um einen Verweis auf die Zelle ScaleY anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Scaley  <br/> |
   
Um einen Verweis auf die Zelle ScaleY anhand des Indexes aus einem Programm abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesScaleY** <br/> |
   

