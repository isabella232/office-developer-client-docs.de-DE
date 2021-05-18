---
title: Zelle "OutputFormat" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251617
localization_priority: Normal
ms.assetid: 17238019-c800-5d3a-32f6-fb0008d4e25f
description: Legt das Ausgabeformat für eine Zeichnung fest. Zeichenblätter werden normalerweise für den Ausdruck formatiert (Standardeinstellung). Sie können jedoch auch andere Ausgabeformate auswählen.
ms.openlocfilehash: 09fa34095772936ab1c6a3025ed1884a533f55e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413885"
---
# <a name="outputformat-cell-document-properties-section"></a>Zelle "OutputFormat" (Abschnitt "Document Properties")

Legt das Ausgabeformat für eine Zeichnung fest. Zeichenblätter werden normalerweise für den Ausdruck formatiert (Standardeinstellung). Sie können jedoch auch andere Ausgabeformate auswählen.
  
|**Wert**|**Ausgabeformat**|
|:-----|:-----|
| 0  <br/> | Drucken (Standard)  <br/> |
| 1  <br/> | PowerPoint-Präsentation  <br/> |
| 2  <br/> | HTML- oder GIF-Ausgabe  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die OutputFormat-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | OutputFormat  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die OutputFormat-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocOutputFormat** <br/> |
   

