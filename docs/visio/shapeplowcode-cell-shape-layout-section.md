---
title: Zelle "ShapePlowCode" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
ms.localizationpriority: medium
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: Legt fest, ob dieses platzierbare Shape verschoben wird, wenn Sie ein anderes platzierbares Shape in der Nähe dieses Shapes auf dem Zeichenblatt ablegen.
ms.openlocfilehash: 53b13a7194bf723410e739b83378fd49e13022c6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622914"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a>Zelle "ShapePlowCode" (Abschnitt "Shape Layout")

Legt fest, ob dieses platzierbare Shape verschoben wird, wenn Sie ein anderes platzierbares Shape in der Nähe dieses Shapes auf dem Zeichenblatt ablegen.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Verschieben nach Blattvorgabe.  <br/> |**visSLOPlowDefault** <br/> |
|1  <br/> |Keine Shapes verschieben.  <br/> |**visSLOPlowNever** <br/> |
|2  <br/> |Jedes Shape verschieben.  <br/> |**visSLOPlowAlways** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch für ein bestimmtes Shape auf der Registerkarte **"Platzierung"** im Dialogfeld **"Verhalten"** festlegen (wenn ein Shape auf der Registerkarte ["Entwickler"](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **"Shape-Entwurf"** ausgewählt ist, klicken Sie auf **"Verhalten",** und klicken Sie dann auf die Registerkarte **"Platzierung").** 
  
Verwenden Sie die Zelle PlowCode im Abschnitt Seitenlayout, um dieses Verhalten für  *alle*  Formen auf dem Zeichenblatt festzulegen. 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "ShapePlowCode" anhand des Namens aus einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapePlowCode  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapePlowCode anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOPlowCode** <br/> |
   

