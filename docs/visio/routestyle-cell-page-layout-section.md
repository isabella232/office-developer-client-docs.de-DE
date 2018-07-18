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
ms.openlocfilehash: d64e7b3c7cf30f0a657ede57b227acefd4b10101
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797895"
---
# <a name="routestyle-cell-page-layout-section"></a>RouteStyle Cell (Page Layout Section)

Legt das Routingformat und die Richtung für sämtliche Verbinder auf dem Zeichenblatt fest, die kein lokales Routingformat haben.
  
|**Wert**|**Routingformat**|**Direction**|**Automatisierungskonstante**|
|:-----|:-----|:-----|:-----|
|0  <br/> |Standard, rechter Winkel  <br/> |Keine  <br/> |**visLORouteDefault** <br/> |
|1  <br/> |Rechter Winkel  <br/> |Keine  <br/> |**visLORouteRightAngle** <br/> |
|2  <br/> |Gerade  <br/> |Keine  <br/> |**visLORouteStraight** <br/> |
|3  <br/> |Organigramm  <br/> |Von oben nach unten  <br/> |**visLORouteOrgChartNS** <br/> |
|4  <br/> |Organigramm  <br/> |Von links nach rechts  <br/> |**visLORouteOrgChartWE** <br/> |
|5  <br/> |Flussdiagramm  <br/> |Von oben nach unten  <br/> |**visLORouteFlowchartNS** <br/> |
|6  <br/> |Flussdiagramm  <br/> |Von links nach rechts  <br/> |**visLORouteFlowchartWE** <br/> |
|7  <br/> |Baum  <br/> |Von oben nach unten  <br/> |**visLORouteTreeNS** <br/> |
|8  <br/> |Baum  <br/> |Von links nach rechts  <br/> |**visLORouteTreeWE** <br/> |
|9  <br/> |Netzwerk  <br/> |Keine  <br/> |**visLORouteNetwork** <br/> |
|10  <br/> |Organigramm  <br/> |Von unten nach oben  <br/> |**visLORouteOrgChartSN** <br/> |
|11  <br/> |Organigramm  <br/> |Von rechts nach links  <br/> |**visLORouteOrgChartEW** <br/> |
|12  <br/> |Flussdiagramm  <br/> |Von unten nach oben  <br/> |**visLORouteFlowchartSN** <br/> |
|13  <br/> |Flussdiagramm  <br/> |Von rechts nach links  <br/> |**visLORouteFlowchartEW** <br/> |
|14  <br/> |Baum  <br/> |Von unten nach oben  <br/> |**visLORouteTreeSN** <br/> |
|15  <br/> |Baum  <br/> |Von rechts nach links  <br/> |**visLORouteTreeEW** <br/> |
|16  <br/> |Mitte an Mitte  <br/> |Keine  <br/> |**visLORouteCenterToCenter** <br/> |
|17  <br/> |Einfach  <br/> |Von oben nach unten  <br/> |**visLORouteSimpleNS** <br/> |
|18  <br/> |Einfach  <br/> |Von links nach rechts  <br/> |**visLORouteSimpleWE** <br/> |
|19  <br/> |Einfach  <br/> |Von unten nach oben  <br/> |**visLORouteSimpleSN** <br/> |
|20  <br/> |Einfach  <br/> |Von rechts nach links  <br/> |**visLORouteSimpleEW** <br/> |
|21  <br/> |Einfach horizontal-vertikal  <br/> |Keine  <br/> |**visLORouteSimpleHV** <br/> |
|22  <br/> |Einfach vertikal-horizontal  <br/> |Keine  <br/> |**visLORouteSimpleVH** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch festlegen, auf der Registerkarte **Layout und Routing** im Dialogfeld **Seite einrichten** (klicken Sie auf der Registerkarte **Entwurf** klicken Sie auf den Pfeil neben **Seite einrichten** , klicken Sie auf **Layout und Routing**und klicken Sie dann auf **Abstand** ). 
  
Sie können ein lokales Routingformat für einen Verbinder in der Zelle ShapeRouteStyle im Abschnitt Shape Layout festlegen. 
  
Wenn Sie einen Verweis auf die Zelle RouteStyle aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |RouteStyle  <br/> |
   
Wenn Sie einen Verweis auf die Zelle RouteStyle aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLORouteStyle** <br/> |
   

