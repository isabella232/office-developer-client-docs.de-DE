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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357267"
---
# <a name="invisible-cell-shape-data-section"></a>Zelle "Invisible" (Abschnitt "Shape Data")

Gibt an, ob das Shape-Datenelement im Fenster **Shape-Daten** angezeigt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shape-Datenelement wird nicht angezeigt.  <br/> |
| FALSE  <br/> | Shape-Datenelement wird angezeigt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert in dieser Zelle entspricht dem Kontrollkästchen **Ausgeblendet** im Dialogfeld **Shape-Daten definieren** (klicken Sie mit der rechten Maustaste auf das Shape, zeigen Sie auf **Daten**, und klicken Sie dann auf **Shape-Daten definieren**).
  
Wenn Sie einen Verweis auf die Zelle inVisible aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Prop.  *Name* . Unsichtbar, wobei Prop.  *Name* ist der Name der Zeile  <br/> |
   
Wenn Sie einen Verweis auf die unsichtbare Zelle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionProp** <br/> |
| Zeilenindex:  <br/> |**visRowProp** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCustPropsInvis** <br/> |
   

