---
title: Zelle "LineWeight" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
ms.localizationpriority: medium
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: Legt die Linienbreite eines Shapes fest. Definieren Sie die Linienbreite, indem Sie eine Zahl mit einer gültigen Maßeinheit eingeben.
ms.openlocfilehash: c38e1b2736c409e3362586bc651a4815394511ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618637"
---
# <a name="lineweight-cell-line-format-section"></a>Zelle "LineWeight" (Abschnitt "Line Format")

Legt die Linienbreite eines Shapes fest. Definieren Sie die Linienbreite, indem Sie eine Zahl mit einer gültigen Maßeinheit eingeben.
  
## <a name="remarks"></a>Bemerkungen

Sie können den Wert von LineWeight auch im Dialogfeld **Linie** festlegen (klicken Sie auf der Registerkarte **"Start"** in der Gruppe **"Shape"** auf **"Linie",** zeigen Sie auf **"Gewichtung",** und klicken Sie dann auf **"Weitere Linien").**
  
Wenn die Maßeinheit nicht eingegeben wird, wird die Maßeinheit für Text verwendet, der im Dialogfeld **Visio Optionen** angegeben ist (klicken Sie auf die Registerkarte **"Datei"** und dann auf **"Optionen").** Die Linienbreite ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt die Linienbreite unverändert. 
  
Um einen Verweis auf die Zelle "LineWeight" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LineWeight  <br/> |
   
Um einen Verweis auf die Zelle "LineWeight" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLine** <br/> |
| Zellenindex:  <br/> |**visLineWeight** <br/> |
   

