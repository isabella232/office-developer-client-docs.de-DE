---
title: Zelle "PaperKind" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
ms.localizationpriority: medium
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: Gibt den Papiertyp für den Druck der Seite an.
ms.openlocfilehash: ccf0118cc5e951a441f904e9920bfa32ef9a251e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608116"
---
# <a name="paperkind-cell-print-properties-section"></a>Zelle "PaperKind" (Abschnitt "Print Properties")

Gibt den Papiertyp für den Druck der Seite an.
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Einstellung entspricht der Einstellung **"Papierformat"** im Dialogfeld **"Druckeinrichtung"** (klicken Sie auf der Registerkarte **"Entwurf"** auf den Pfeil **"Seite einrichten",** und klicken Sie dann auf der Registerkarte **"Druckeinrichtung"** auf die Schaltfläche **"Einrichten").** 
  
Die numerischen Werte in dieser Zelle entsprechen Konstanten (mit dem Präfix DMPAPER), die für die Papierauswahl in der Datei Microsoft Windows wingdi.h definiert sind. 
  
Um einen Verweis auf die Zelle PaperKind anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PaperKind  <br/> |
   
Um einen Verweis auf die Zelle PaperKind anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesPaperKind** <br/> |
   

