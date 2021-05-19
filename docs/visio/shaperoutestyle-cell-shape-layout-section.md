---
title: Zelle "ShapeRouteStyle" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm905
localization_priority: Normal
ms.assetid: a5dcd2e0-e343-5ee2-2b63-2a1312437901
description: Legt das Routingformat und die Richtung für einen ausgewählten Verbinder auf dem Zeichenblatt fest.
ms.openlocfilehash: e5725d461a71dad4623161d99134a20250abe724
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425029"
---
# <a name="shaperoutestyle-cell-shape-layout-section"></a>Zelle "ShapeRouteStyle" (Abschnitt "Shape Layout")

Legt das Routingformat und die Richtung für einen ausgewählten Verbinder auf dem Zeichenblatt fest.
  
|**Wert**|**Routingformat**|**Richtung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|:-----|
|0  <br/> |Zeichenblattstandard verwenden  <br/> |Keine  <br/> |**visLORouteDefault** <br/> |
|1  <br/> |Rechter Winkel  <br/> |Keine  <br/> |**visLORouteRightAngle** <br/> |
|2  <br/> |Straight  <br/> |Keine  <br/> |**visLORouteStraight** <br/> |
|3  <br/> |Organigramm  <br/> |Von oben nach unten  <br/> |**visLORouteOrgChartNS** <br/> |
|4   <br/> |Organigramm  <br/> |Von links nach rechts  <br/> |**visLORouteOrgChartWE** <br/> |
|5   <br/> |Flussdiagramm  <br/> |Von oben nach unten  <br/> |**visLORouteFlowchartNS** <br/> |
|6   <br/> |Flussdiagramm  <br/> |Von links nach rechts  <br/> |**visLORouteFlowchartWE** <br/> |
|7   <br/> |Struktur  <br/> |Von oben nach unten  <br/> |**visLORouteTreeNS** <br/> |
|8   <br/> |Struktur  <br/> |Von links nach rechts  <br/> |**visLORouteTreeWE** <br/> |
|9   <br/> |Netzwerk  <br/> |Keine  <br/> |**visLORouteNetwork** <br/> |
|10  <br/> |Organigramm  <br/> |Von unten nach oben  <br/> |**visLORouteOrgChartSN** <br/> |
|11  <br/> |Organigramm  <br/> |Von rechts nach links  <br/> |**visLORouteOrgChartEW** <br/> |
|12   <br/> |Flussdiagramm  <br/> |Von unten nach oben  <br/> |**visLORouteFlowchartSN** <br/> |
|13  <br/> |Flussdiagramm  <br/> |Von rechts nach links  <br/> |**visLORouteFlowchartEW** <br/> |
|14   <br/> |Struktur  <br/> |Von unten nach oben  <br/> |**visLORouteTreeSN** <br/> |
|15   <br/> |Struktur  <br/> |Von rechts nach links  <br/> |**visLORouteTreeEW** <br/> |
|16   <br/> |Mitte an Mitte  <br/> |Keine  <br/> |**visLORouteCenterToCenter** <br/> |
|17   <br/> |Einfach  <br/> |Von oben nach unten  <br/> |**visLORouteSimpleNS** <br/> |
|18   <br/> |Einfach  <br/> |Von links nach rechts  <br/> |**visLORouteSimpleWE** <br/> |
|19  <br/> |Einfach  <br/> |Von unten nach oben  <br/> |**visLORouteSimpleSN** <br/> |
|20  <br/> |Einfach  <br/> |Von rechts nach links  <br/> |**visLORouteSimpleEW** <br/> |
| 21  <br/> |Einfach horizontal-vertikal  <br/> |Keine  <br/> |**visLORouteSimpleHV** <br/> |
|22  <br/> |Einfach vertikal-horizontal  <br/> |Keine  <br/> |**visLORouteSimpleVH** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können den Wert dieser Zelle für einen bestimmten  Connector auch auf der Registerkarte  **Connector** im [](run-in-developer-mode-display-the-developer-tab.md) Dialogfeld Verhalten festlegen (wenn ein Connector ausgewählt ist, klicken Sie auf der Registerkarte Entwickler auf Verhalten, und klicken Sie dann auf die Registerkarte **Connector).** 
  
Verwenden Sie zum Festlegen dieses Verhaltens für  *alle*  Connectors auf einer Seite die Zelle RouteStyle im Abschnitt Seitenlayout. 
  
In Versionen vor Visio  2000 wird dieses Verhalten in der Zelle ObjVerhalten im Abschnitt Miscellaneous festgelegt.
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle ShapeRouteStyle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapeRouteStyle  <br/> |
   
Um einen Verweis auf die Zelle ShapeRouteStyle nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLORouteStyle** <br/> |
   

