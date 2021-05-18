---
title: Zelle "LineWeight" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
localization_priority: Normal
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: Legt die Linienbreite eines Shapes fest. Definieren Sie die Linienbreite, indem Sie eine Zahl mit einer gültigen Maßeinheit eingeben.
ms.openlocfilehash: 654a93f939226bedab2e40ab591dad0e3f872267
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412247"
---
# <a name="lineweight-cell-line-format-section"></a>Zelle "LineWeight" (Abschnitt "Line Format")

Legt die Linienbreite eines Shapes fest. Definieren Sie die Linienbreite, indem Sie eine Zahl mit einer gültigen Maßeinheit eingeben.
  
## <a name="remarks"></a>Hinweise

Sie können den Wert von LineWeight auch im  Dialogfeld Linie festlegen (klicken Sie auf der Registerkarte Start in der **Gruppe Shape** auf **Linie,** zeigen Sie auf **Gewichtung,** und klicken Sie dann auf **Weitere Linien**). 
  
Wenn die Maßeinheit nicht eingegeben wird, wird die Maßeinheit für text verwendet, die  im Dialogfeld **Visio Optionen** angegeben ist (klicken Sie auf die Registerkarte Datei, und klicken Sie dann auf **Optionen**). Die Linienbreite ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt die Linienbreite unverändert. 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle LineWeight anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LineWeight  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LineWeight-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLine** <br/> |
| Zellenindex:  <br/> |**visLineWeight** <br/> |
   

