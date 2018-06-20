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
ms.openlocfilehash: 2cd3fcad5db7b1752c55055354f1ec842bff4899
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797215"
---
# <a name="invisible-cell-shape-data-section"></a>Invisible Cell (Shape Data Section)

Gibt an, ob das Shape-Datenelement im Fenster **Shape-Daten** angezeigt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shape-Datenelement wird nicht angezeigt.  <br/> |
| FALSE  <br/> | Shape-Datenelement wird angezeigt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert in dieser Zelle entspricht dem Kontrollkästchen **ausgeblendet** im Dialogfeld **Shape-Daten definieren** (mit der rechten Maustaste in des Shapes, zeigen Sie auf **Daten**, und klicken Sie dann auf **Shape-Daten definieren**).
  
Wenn Sie einen Verweis auf die Zelle Invisible nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Eigenschaft.  *Name* . Nicht sichtbare Where Prop.  *Name* ist der Zeilenname  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Invisible aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionProp** <br/> |
| Zeilenindex:  <br/> |**VisRowProp** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCustPropsInvis** <br/> |
   

