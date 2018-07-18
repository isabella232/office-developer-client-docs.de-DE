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
ms.openlocfilehash: 23887e1d265e9e5ac1dfa9750bab65e8428b1c76
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797572"
---
# <a name="objtype-cell-miscellaneous-section"></a>ObjType Cell (Miscellaneous Section)

Legt fest, ob Objekte in Diagrammen platzierbar oder umleitbar sind, wenn Shapes mithilfe des Dialogfelds **Layout konfigurieren** ausgerichtet werden. 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |Standardeinstellung. Die Anwendung entscheidet diesen Punkt abhängig vom Zeichnungskontext.  <br/> |**visLOFlagsVisDecides** <br/> |
|&amp;H1  <br/> |Shape ist platzierbar.  <br/> |**visLOFlagsPlacable** <br/> |
|&amp;H2  <br/> |Shape ist umleitbar. Es muss sich jedoch um ein eindimensionales Shape (1D-Shape) handeln.  <br/> |**visLOFlagsRoutable** <br/> |
|&amp;H4  <br/> |Shape ist weder platzierbar noch umleitbar.  <br/> |**visLOFlagsDont** <br/> |
|&amp;H8  <br/> |Gruppe enthält platzierbare oder umleitbare Shapes.  <br/> |**visLOFlagsPNRGroup** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Standardmäßig ist die Zelle ObjType für ein Shape auf Keine Formel (also gleich 0) gesetzt, was bedeutet, dass die Anwendung bestimmt, ob das Shape in Abhängigkeit von seinem Kontext platziert werden kann. Wenn Sie beispielsweise ein einfaches Rechteck zeichnen, lautet der Wert in der Zelle ObjType 0 (Null). Wenn Sie daraufhin das Tool Automatischer Verbinder verwenden, um das Rechteck mit einem anderen Shape zu verbinden, setzt Visio den Wert der Zelle ObjType für dieses Rechteck auf 1 (platzierbar). 
  
Der Wert der Zelle ObjType kann eine Kombination von Werten sein. Wenn das nicht platzierbare Bit festgelegt ist (&amp;H4), jedoch, er hat Vorrang vor anderen Werten mit Ausnahme der Gruppenwert (&amp;H8).
  
Wenn Sie einen Verweis auf die Zelle ObjType aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ObjType  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ObjType aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowMisc** <br/> |
|Zellenindex:  <br/> |**visLOFlags** <br/> |
   

