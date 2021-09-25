---
title: Zelle "OutputFormat" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251617
ms.localizationpriority: medium
ms.assetid: 17238019-c800-5d3a-32f6-fb0008d4e25f
description: Legt das Ausgabeformat für eine Zeichnung fest. Zeichenblätter werden normalerweise für den Ausdruck formatiert (Standardeinstellung). Sie können jedoch auch andere Ausgabeformate auswählen.
ms.openlocfilehash: b4e2c63912509c9cdae04f828e138ef90fbe4859
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577815"
---
# <a name="outputformat-cell-document-properties-section"></a>Zelle "OutputFormat" (Abschnitt "Document Properties")

Legt das Ausgabeformat für eine Zeichnung fest. Zeichenblätter werden normalerweise für den Ausdruck formatiert (Standardeinstellung). Sie können jedoch auch andere Ausgabeformate auswählen.
  
|**Wert**|**Ausgabeformat**|
|:-----|:-----|
| 0  <br/> | Drucken (Standard)  <br/> |
| 1  <br/> | PowerPoint-Präsentation  <br/> |
| 2  <br/> | HTML- oder GIF-Ausgabe  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie Folgendes, um einen Verweis auf die Zelle "OutputFormat" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | OutputFormat  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "OutputFormat" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocOutputFormat** <br/> |
   

