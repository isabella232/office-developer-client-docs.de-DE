---
title: Zelle "PaperSource" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60068
ms.localizationpriority: medium
ms.assetid: 771a2ab4-578d-51c3-fabd-138f7952bb11
description: Bestimmt die Papierzufuhr für die Seite.
ms.openlocfilehash: 90d9013ebd831851d42b55dc4f1d754f9dc4c5cc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598444"
---
# <a name="papersource-cell-printproperties-section"></a>Zelle "PaperSource" (Abschnitt "Print Properties")

Bestimmt die Papierzufuhr für die Seite. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Einstellung entspricht der Einstellung **Papierzufuhr** im Dialogfeld **Druckeinrichtung** (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten** und anschließend auf der Registerkarte **Druckeinrichtung** auf **Einrichten**).
  
Die numerischen Werte in dieser Zelle sind Konstanten (mit dem Präfix DMBIN) zugeordnet, die für Bin-Auswahlen in der Datei "Microsoft Windows wingdi.h" definiert sind. Beispielsweise stellt der Wert 7 DMBIN_AUTO dar. 
  
Um einen Verweis auf die Zelle PaperSource anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PaperSource  <br/> |
   
Um einen Verweis auf die Zelle PaperSource anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesPaperSource** <br/> |
   

