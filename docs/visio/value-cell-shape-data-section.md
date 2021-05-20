---
title: Zelle "Value" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1090
localization_priority: Normal
ms.assetid: fd42a6ce-f621-4e9e-aba3-23a1b87a5651
description: Enthält den Wert des Shape-Datenelements, der in das Dialogfeld Shape-Daten definieren eingegeben wurde.
ms.openlocfilehash: 40d9e7fdd92ac8fa800a146ea45bbcd002ace87b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431904"
---
# <a name="value-cell-shape-data-section"></a>Zelle "Value" (Abschnitt "Shape Data")

Enthält den Wert des Shape-Datenelements, der in das Dialogfeld **Shape-Daten definieren** eingegeben wurde. 
  
## <a name="remarks"></a>Hinweise

Die in diese Zelle eingegebenen Formeln werden von den im Dialogfeld **Shape-Daten definieren** eingegebenen Werten überschrieben. Dies gilt auch, wenn Sie die Formel mithilfe der GUARD-Funktion schützen. 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle Value anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Prop.  *Name*  . Wert, wobei Prop.  *Name*  ist der Zeilenname  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Value nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionProp** <br/> |
| Zeilenindex:  <br/> |**visRowProp**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCustPropsValue** <br/> |
   

