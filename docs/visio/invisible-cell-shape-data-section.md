---
title: Zelle "Invisible" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251341
ms.localizationpriority: medium
ms.assetid: 5f368c2e-2a40-38ee-3568-ed5c57633345
description: Gibt an, ob das Shape-Datenelement im Fenster Shape-Daten angezeigt wird.
ms.openlocfilehash: 046ae26940da77297b1671af29ace286314dd730
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582617"
---
# <a name="invisible-cell-shape-data-section"></a>Zelle "Invisible" (Abschnitt "Shape Data")

Gibt an, ob das Shape-Datenelement im Fenster **Shape-Daten** angezeigt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shape-Datenelement wird nicht angezeigt.  <br/> |
| FALSE  <br/> | Shape-Datenelement wird angezeigt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert in dieser Zelle entspricht dem Kontrollkästchen **Ausgeblendet** im Dialogfeld **Shape-Daten definieren** (klicken Sie mit der rechten Maustaste auf das Shape, zeigen Sie auf **Daten**, und klicken Sie dann auf **Shape-Daten definieren**).
  
Um einen Verweis auf die Zelle "Invisible" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Prop.  *Name*  . Unsichtbar, wo Prop.  *Name*  ist der Zeilenname  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "Invisible" anhand des Indexes aus einem Programm abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionProp** <br/> |
| Zeilenindex:  <br/> |**visRowProp**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCustPropsInvis** <br/> |
   

