---
title: Zelle "Value" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1090
ms.localizationpriority: medium
ms.assetid: fd42a6ce-f621-4e9e-aba3-23a1b87a5651
description: Enthält den Wert des Shape-Datenelements, der in das Dialogfeld Shape-Daten definieren eingegeben wurde.
ms.openlocfilehash: 20b9ef754ceadccc0c532c6c7f21f38cdc2ae497
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553662"
---
# <a name="value-cell-shape-data-section"></a>Zelle "Value" (Abschnitt "Shape Data")

Enthält den Wert des Shape-Datenelements, der in das Dialogfeld **Shape-Daten definieren** eingegeben wurde. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die in diese Zelle eingegebenen Formeln werden von den im Dialogfeld **Shape-Daten definieren** eingegebenen Werten überschrieben. Dies gilt auch, wenn Sie die Formel mithilfe der GUARD-Funktion schützen. 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle Value anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Prop.  *Name*  . Wert, wobei Prop.  *Name*  ist der Zeilenname  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Value anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionProp** <br/> |
| Zeilenindex:  <br/> |**visRowProp**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCustPropsValue** <br/> |
   

