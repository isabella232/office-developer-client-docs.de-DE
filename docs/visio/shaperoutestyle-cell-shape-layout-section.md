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
ms.openlocfilehash: b165d43e64842565806d93d620ddbd24f41a2d57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798033"
---
# <a name="shaperoutestyle-cell-shape-layout-section"></a>ShapeRouteStyle Cell (Shape Layout Section)

Legt das Routingformat und die Richtung für einen ausgewählten Verbinder auf dem Zeichenblatt fest.
  
|**Wert**|**Routingformat**|**Direction**|**Automatisierungskonstante**|
|:-----|:-----|:-----|:-----|
|0  <br/> |Zeichenblattstandard verwenden  <br/> |Keine  <br/> |**visLORouteDefault** <br/> |
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

Sie können den Wert dieser Zelle auch auf die Registerkarte **Verbinder** im Dialogfeld **Verhalten** für einen bestimmten Verbinder festlegen (klicken Sie bei markiertem Verbinder, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** , und klicken Sie dann auf die Registerkarte **Verbinder** ). 
  
Wenn Sie dieses Verhalten für *sämtliche* die Verbinder auf einem Zeichenblatt festlegen möchten, verwenden Sie die Zelle RouteStyle im Abschnitt Page Layout. 
  
In Versionen vor Visio  2000 wird dieses Verhalten in der Zelle ObjVerhalten im Abschnitt Miscellaneous festgelegt.
  
Wenn Sie einen Verweis auf die Zelle ShapeRouteStyle aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapeRouteStyle  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ShapeRouteStyle aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLORouteStyle** <br/> |
   

