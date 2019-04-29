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
|&amp;H0  <br/> |Standardwert. Die Anwendung entscheidet diesen Punkt abhängig vom Zeichnungskontext.  <br/> |**visLOFlagsVisDecides** <br/> |
|&amp;H1  <br/> |Shape ist platzierbar.  <br/> |**visLOFlagsPlacable** <br/> |
|&amp;H2  <br/> |Shape ist umleitbar. Es muss sich jedoch um ein eindimensionales Shape (1D-Shape) handeln.  <br/> |**visLOFlagsRoutable** <br/> |
|&amp;H4  <br/> |Shape ist weder platzierbar noch umleitbar.  <br/> |**visLOFlagsDont** <br/> |
|&amp;H8  <br/> |Gruppe enthält platzierbare oder umleitbare Shapes.  <br/> |**visLOFlagsPNRGroup** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Standardmäßig ist die Zelle ObjType-Zelle auf keine Formel für eine Form festgelegt, die auf 0 ausgewertet wird, was bedeutet, dass die Anwendung bestimmt, ob das Shape abhängig vom Kontext platziert werden kann. Wenn Sie beispielsweise ein einfaches Rechteck zeichnen, ist der Wert der Zelle ObjType-Zelle 0. Wenn Sie das Rechteck mit **** einem anderen Shape verbinden, setzt Visio den Wert der Zelle Zelle ObjType des Rechtecks auf 1 (placeable) zurück. 
  
Der Wert der Zelle ObjType kann eine Kombination aus mehreren verschiedenen Werten sein. Wenn das nicht platzierte Bit (&amp;H4) festgelegt ist, hat es Vorrang vor anderen Werten mit Ausnahme des Group-Werts (&amp;H8).
  
Wenn Sie einen Verweis auf die Zelle Zelle ObjType aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle ObjType  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ObjType aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowMisc** <br/> |
|Zellenindex:  <br/> |**visLOFlags** <br/> |
   

