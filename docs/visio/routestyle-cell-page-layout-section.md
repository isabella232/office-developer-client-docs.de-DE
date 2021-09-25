---
title: Zelle "RouteStyle" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251662
ms.localizationpriority: medium
ms.assetid: 3a223dac-538b-cb5d-a32d-61395276f9da
description: Legt das Routingformat und die Richtung für sämtliche Verbinder auf dem Zeichenblatt fest, die kein lokales Routingformat haben.
ms.openlocfilehash: aa7979183e4e717ef7432c74b8f998274b5a48e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573509"
---
# <a name="routestyle-cell-page-layout-section"></a>Zelle "RouteStyle" (Abschnitt "Page Layout")

Legt das Routingformat und die Richtung für sämtliche Verbinder auf dem Zeichenblatt fest, die kein lokales Routingformat haben.
  
|**Wert**|**Routingformat**|**Direction**|**Automatisierungskonstante**|
|:-----|:-----|:-----|:-----|
|0  <br/> |Standard, rechter Winkel  <br/> |Keines  <br/> |**visLORouteDefault** <br/> |
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

Sie können den Wert dieser Zelle auch auf der Registerkarte **Layout und** Routing im Dialogfeld Seite einrichten festlegen (klicken Sie auf der Registerkarte Entwurf auf den Pfeil neben Seite **einrichten,** auf Layout **und Routing und** anschließend auf Abstand ).    
  
Sie können ein lokales Routingformat für einen Verbinder in der Zelle ShapeRouteStyle im Abschnitt Shape Layout festlegen. 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "RouteStyle" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |RouteStyle  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle RouteStyle anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLORouteStyle** <br/> |
   

