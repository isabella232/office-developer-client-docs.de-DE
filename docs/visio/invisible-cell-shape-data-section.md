---
title: Zelle "Invisible" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251341
localization_priority: Normal
ms.assetid: 5f368c2e-2a40-38ee-3568-ed5c57633345
description: Gibt an, ob das Shape-Datenelement im Fenster Shape-Daten angezeigt wird.
ms.openlocfilehash: 8671fcc249b7ca81c011f697721093e7842c1558
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405317"
---
# <a name="invisible-cell-shape-data-section"></a>Zelle "Invisible" (Abschnitt "Shape Data")

Gibt an, ob das Shape-Datenelement im Fenster **Shape-Daten** angezeigt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shape-Datenelement wird nicht angezeigt.  <br/> |
| FALSE  <br/> | Shape-Datenelement wird angezeigt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert in dieser Zelle entspricht dem Kontrollkästchen **Ausgeblendet** im Dialogfeld **Shape-Daten definieren** (klicken Sie mit der rechten Maustaste auf das Shape, zeigen Sie auf **Daten**, und klicken Sie dann auf **Shape-Daten definieren**).
  
Um einen Verweis auf die Zelle Invisible anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Prop.  *Name*  . Unsichtbar, wo Prop.  *Name*  ist der Zeilenname  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Invisible nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionProp** <br/> |
| Zeilenindex:  <br/> |**visRowProp**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCustPropsInvis** <br/> |
   

