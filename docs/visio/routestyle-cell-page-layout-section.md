---
title: Zelle "RouteStyle" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251662
localization_priority: Normal
ms.assetid: 3a223dac-538b-cb5d-a32d-61395276f9da
description: Legt das Routingformat und die Richtung für sämtliche Verbinder auf dem Zeichenblatt fest, die kein lokales Routingformat haben.
ms.openlocfilehash: 38de871460c155ee5d495599a239ebeb0ff1c33d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424784"
---
# <a name="routestyle-cell-page-layout-section"></a>Zelle "RouteStyle" (Abschnitt "Page Layout")

Legt das Routingformat und die Richtung für sämtliche Verbinder auf dem Zeichenblatt fest, die kein lokales Routingformat haben.
  
|**Wert**|**Routingformat**|**Richtung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|:-----|
|0  <br/> |Standard, rechter Winkel  <br/> |Keine  <br/> |**visLORouteDefault** <br/> |
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

Sie können den Wert dieser Zelle auch auf der  Registerkarte **Layout** und  Routing im Dialogfeld  Seiteneinrichtung festlegen (klicken Sie auf der Registerkarte Entwurf auf den Pfeil Seite einrichten, klicken Sie auf Layout und **Routing** und dann auf **Abstand** ). 
  
Sie können ein lokales Routingformat für einen Verbinder in der Zelle ShapeRouteStyle im Abschnitt Shape Layout festlegen. 
  
Um einen Verweis auf die Zelle RouteStyle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |RouteStyle  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle RouteStyle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLORouteStyle** <br/> |
   

