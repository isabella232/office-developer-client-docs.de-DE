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
ms.openlocfilehash: eb6e7daccb1743c43a30b34598e47187496e4aac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406759"
---
# <a name="papersource-cell-printproperties-section"></a>Zelle "PaperSource" (Abschnitt "Print Properties")

Bestimmt die Papierzufuhr für die Seite. 
  
## <a name="remarks"></a>Hinweise

Diese Einstellung entspricht der Einstellung **Papierzufuhr** im Dialogfeld **Druckeinrichtung** (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten** und anschließend auf der Registerkarte **Druckeinrichtung** auf **Einrichten**).
  
Die numerischen Werte in dieser Zelle ordnen Konstanten (mit DMBIN vorangestellt) zu, die für die Binauswahl in der Datei "Microsoft Windows wingdi.h" definiert sind. Beispielsweise steht der Wert 7 für DMBIN_AUTO. 
  
Um einen Verweis auf die Zelle PaperSource anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PaperSource  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PaperSource nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesPaperSource** <br/> |
   

