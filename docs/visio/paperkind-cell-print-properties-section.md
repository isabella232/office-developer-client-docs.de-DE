---
title: Zelle "PaperKind" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
localization_priority: Normal
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: Gibt den Papiertyp für den Druck der Seite an.
ms.openlocfilehash: 694aa1fb8b52f5ae323c47e9aab8715b4a48dfb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408446"
---
# <a name="paperkind-cell-print-properties-section"></a>Zelle "PaperKind" (Abschnitt "Print Properties")

Gibt den Papiertyp für den Druck der Seite an.
  
## <a name="remarks"></a>Hinweise

Diese Einstellung entspricht  der Einstellung Papierformat im Dialogfeld  Druckeinrichtung (klicken  Sie auf der Registerkarte  Entwurf auf den Pfeil Seite einrichten, und klicken Sie dann auf der Registerkarte Druckeinrichtung auf die Schaltfläche **Setup).**  
  
Die numerischen Werte in dieser Zelle ordnen Konstanten (mit DMPAPER vorangestellt) zu, die für die Papierauswahl in der Datei "Microsoft Windows wingdi.h" definiert sind. 
  
Um einen Verweis auf die Zelle PaperKind anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PaperKind  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PaperKind nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesPaperKind** <br/> |
   

