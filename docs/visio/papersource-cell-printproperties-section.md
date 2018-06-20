---
title: Zelle "PaperSource" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60068
localization_priority: Normal
ms.assetid: 771a2ab4-578d-51c3-fabd-138f7952bb11
description: Bestimmt die Papierzufuhr für die Seite.
ms.openlocfilehash: f1dedf210dfe0dd8cac3d36fdec03fb497f6572c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797593"
---
# <a name="papersource-cell-printproperties-section"></a>PaperSource Cell (PrintProperties Section)

Bestimmt die Papierzufuhr für die Seite. 
  
## <a name="remarks"></a>Bemerkungen

Diese Einstellung entspricht der Einstellung **Papierzufuhr** im Dialogfeld **Drucker einrichten** (klicken Sie auf der Registerkarte **Entwurf** , klicken Sie auf den Pfeil neben **Seite einrichten** , und klicken Sie dann auf der Registerkarte **Drucken Setup** auf **Setup**).
  
Die numerischen Werte in dieser Zelle auf Konstanten (mit dem Präfix DMBIN) in der Microsoft Windows-Datei wingdi.h definiert; Beispielsweise steht für den Wert 7 Papierauswahl. 
  
Wenn Sie einen Verweis auf die Zelle PaperSource nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PaperSource  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PaperSource aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesPaperSource** <br/> |
   

