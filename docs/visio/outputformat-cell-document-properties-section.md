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
description: Bestimmt das Ausgabeformat für eine Zeichnung. Zeichnungs Seiten sind normalerweise zum Drucken formatiert (Standard); Sie können jedoch auch andere Ausgabeformate auswählen.
ms.openlocfilehash: 09fa34095772936ab1c6a3025ed1884a533f55e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359283"
---
# <a name="outputformat-cell-document-properties-section"></a>Zelle "OutputFormat" (Abschnitt "Document Properties")

Bestimmt das Ausgabeformat für eine Zeichnung. Zeichnungs Seiten sind normalerweise zum Drucken formatiert (Standard); Sie können jedoch auch andere Ausgabeformate auswählen.
  
|**Wert**|**Ausgabeformat**|
|:-----|:-----|
| 0  <br/> | Drucken (Standard)  <br/> |
| 1  <br/> | PowerPoint-Präsentation  <br/> |
| 2  <br/> | HTML- oder GIF-Ausgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle OutputFormat aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | OutputFormat  <br/> |
   
Wenn Sie einen Verweis auf die Zelle OutputFormat aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocOutputFormat** <br/> |
   

