---
title: Zelle "ShapeRouteStyle" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm905
ms.localizationpriority: medium
ms.assetid: a5dcd2e0-e343-5ee2-2b63-2a1312437901
description: Legt das Routingformat und die Richtung für einen ausgewählten Verbinder auf dem Zeichenblatt fest.
ms.openlocfilehash: cb927357ce2ad0d7740708b1bafd93b64ce2135b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573306"
---
# <a name="shaperoutestyle-cell-shape-layout-section"></a>Zelle "ShapeRouteStyle" (Abschnitt "Shape Layout")

Legt das Routingformat und die Richtung für einen ausgewählten Verbinder auf dem Zeichenblatt fest.
  
|**Wert**|**Routingformat**|**Direction**|**Automatisierungskonstante**|
|:-----|:-----|:-----|:-----|
|0  <br/> |Zeichenblattstandard verwenden  <br/> |Keines  <br/> |**visLORouteDefault** <br/> |
|1  <br/> |Rechter Winkel  <br/> |Keines  <br/> |**visLORouteRightAngle** <br/> |
|2  <br/> |Gerade  <br/> |Keines  <br/> |**visLORouteStraight** <br/> |
|3  <br/> |Organigramm  <br/> |Von oben nach unten  <br/> |**visLORouteOrgChartNS** <br/> |
|4   <br/> |Organigramm  <br/> |Von links nach rechts  <br/> |**visLORouteOrgChartWE** <br/> |
|5  <br/> |Flussdiagramm  <br/> |Von oben nach unten  <br/> |**visLORouteFlowchartNS** <br/> |
|6   <br/> |Flussdiagramm  <br/> |Von links nach rechts  <br/> |**visLORouteFlowchartWE** <br/> |
|7   <br/> |Baum  <br/> |Von oben nach unten  <br/> |**visLORouteTreeNS** <br/> |
|8   <br/> |Baum  <br/> |Von links nach rechts  <br/> |**visLORouteTreeWE** <br/> |
|9   <br/> |Netzwerk  <br/> |Keines  <br/> |**visLORouteNetwork** <br/> |
|10  <br/> |Organigramm  <br/> |Von unten nach oben  <br/> |**visLORouteOrgChartSN** <br/> |
|11  <br/> |Organigramm  <br/> |Von rechts nach links  <br/> |**visLORouteOrgChartEW** <br/> |
|12   <br/> |Flussdiagramm  <br/> |Von unten nach oben  <br/> |**visLORouteFlowchartSN** <br/> |
|13  <br/> |Flussdiagramm  <br/> |Von rechts nach links  <br/> |**visLORouteFlowchartEW** <br/> |
|14   <br/> |Baum  <br/> |Von unten nach oben  <br/> |**visLORouteTreeSN** <br/> |
|15   <br/> |Baum  <br/> |Von rechts nach links  <br/> |**visLORouteTreeEW** <br/> |
|16   <br/> |Mitte an Mitte  <br/> |Keines  <br/> |**visLORouteCenterToCenter** <br/> |
|17   <br/> |Einfach  <br/> |Von oben nach unten  <br/> |**visLORouteSimpleNS** <br/> |
|18   <br/> |Einfach  <br/> |Von links nach rechts  <br/> |**visLORouteSimpleWE** <br/> |
|19  <br/> |Einfach  <br/> |Von unten nach oben  <br/> |**visLORouteSimpleSN** <br/> |
|20  <br/> |Einfach  <br/> |Von rechts nach links  <br/> |**visLORouteSimpleEW** <br/> |
| 21  <br/> |Einfach horizontal-vertikal  <br/> |Keines  <br/> |**visLORouteSimpleHV** <br/> |
|22  <br/> |Einfach vertikal-horizontal  <br/> |Keines  <br/> |**visLORouteSimpleVH** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können den Wert dieser Zelle für einen bestimmten Verbinder auch auf der Registerkarte **"Connector"** im Dialogfeld **"Verhalten"** festlegen (wenn ein Connector ausgewählt ist, klicken Sie auf der Registerkarte ["Entwicklertools"](run-in-developer-mode-display-the-developer-tab.md) auf **"Verhalten",** und klicken Sie dann auf die Registerkarte **"Connector").** 
  
Verwenden Sie die Zelle RouteStyle im Abschnitt Seitenlayout, um dieses Verhalten für  *alle*  Connectors auf einer Seite festzulegen. 
  
In Versionen vor Visio  2000 wird dieses Verhalten in der Zelle ObjVerhalten im Abschnitt Miscellaneous festgelegt.
  
Um einen Verweis auf die Zelle ShapeRouteStyle anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapeRouteStyle  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapeRouteStyle anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLORouteStyle** <br/> |
   

