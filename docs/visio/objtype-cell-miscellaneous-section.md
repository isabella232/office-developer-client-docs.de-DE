---
title: Zelle "ObjType" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm745
localization_priority: Normal
ms.assetid: 3afee07b-e91a-a91c-fba2-0e3251dd6385
description: Legt fest, ob Objekte in Diagrammen platzierbar oder umleitbar sind, wenn Shapes mithilfe des Dialogfelds Layout konfigurieren ausgerichtet werden.
ms.openlocfilehash: 7a607fdb53ad569e84976b6f9911fbd89f7f2628
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425729"
---
# <a name="objtype-cell-miscellaneous-section"></a>Zelle "ObjType" (Abschnitt "Miscellaneous")

Legt fest, ob Objekte in Diagrammen platzierbar oder umleitbar sind, wenn Shapes mithilfe des Dialogfelds **Layout konfigurieren** ausgerichtet werden. 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |Standardeinstellung. Die Anwendung entscheidet diesen Punkt abhängig vom Zeichnungskontext.  <br/> |**visLOFlagsVisDecides** <br/> |
|&amp;H1  <br/> |Shape ist platzierbar.  <br/> |**visLOFlagsPlacable** <br/> |
|&amp;H2  <br/> |Shape ist umleitbar. Es muss sich jedoch um ein eindimensionales Shape (1D-Shape) handeln.  <br/> |**visLOFlagsRoutable** <br/> |
|&amp;H4  <br/> |Shape ist weder platzierbar noch umleitbar.  <br/> |**visLOFlagsDont** <br/> |
|&amp;H8  <br/> |Gruppe enthält platzierbare oder umleitbare Shapes.  <br/> |**visLOFlagsPNRGroup** <br/> |
   
## <a name="remarks"></a>Hinweise

Standardmäßig ist die Zelle ObjType auf Keine Formel für eine Form festgelegt, die auf 0 ausgewertet wird, was bedeutet, dass die Anwendung bestimmt, ob das Shape je nach Kontext platzierbar sein kann. Wenn Sie beispielsweise ein einfaches Rechteck zeichnen, ist der Wert der Zelle ObjType 0. Wenn Sie dann  das Connector-Tool verwenden, um das Rechteck mit einer anderen Form zu verbinden, setzt Visio den Wert der Zelle ObjType des Rechtecks auf 1 (platzierbar) zurück. 
  
Der Wert der Zelle ObjType kann eine Kombination aus mehreren verschiedenen Werten sein. Wenn das nicht platzierbare Bit festgelegt ist ( H4), hat es jedoch Vorrang vor anderen Werten mit Ausnahme des &amp; Gruppenwerts ( &amp; H8).
  
Um einen Verweis auf die Zelle ObjType anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ObjType  <br/> |
   
Um einen Verweis auf die Zelle ObjType nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowMisc** <br/> |
|Zellenindex:  <br/> |**visLOFlags** <br/> |
   

