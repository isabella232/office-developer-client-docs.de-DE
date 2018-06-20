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
description: Enthält das Shape-Datenelement Wert im Dialogfeld Shape-Daten definieren eingegeben wurde.
ms.openlocfilehash: 5b373149360167585fc5a143ce9458703e219045
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798382"
---
# <a name="value-cell-shape-data-section"></a>Zelle "Value" (Abschnitt "Shape Data")

Enthält das Shape-Datenelement Wert im Dialogfeld **Shape-Daten definieren** eingegeben wurde. 
  
## <a name="remarks"></a>Hinweise

In dieser Zelle eingegebenen Formeln werden durch die Werte im Dialogfeld **Shape-Daten definieren** eingegeben überschrieben. Dies gilt auch, wenn Sie die GUARD-Funktion verwenden, um die Formel zu schützen. 
  
Zum Abrufen eines Verweises auf die Zelle Value nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Eigenschaft.  *Name* . Wert wobei Prop.  *Name* ist der Zeilenname  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Value aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionProp** <br/> |
| Zeilenindex:  <br/> |**VisRowProp** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCustPropsValue** <br/> |
   

