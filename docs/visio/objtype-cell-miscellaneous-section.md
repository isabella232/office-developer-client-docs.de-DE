---
title: Zelle "ObjType" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm745
ms.localizationpriority: medium
ms.assetid: 3afee07b-e91a-a91c-fba2-0e3251dd6385
description: Legt fest, ob Objekte in Diagrammen platzierbar oder umleitbar sind, wenn Shapes mithilfe des Dialogfelds Layout konfigurieren ausgerichtet werden.
ms.openlocfilehash: 22a34d21cf383ea12c05bb43588702335ae593ff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608186"
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
   
## <a name="remarks"></a>HinwBemerkungeneise

Standardmäßig ist die Zelle ObjType für ein Shape auf Keine Formel festgelegt, was bedeutet, dass die Anwendung bestimmt, ob das Shape je nach Kontext platzierbar sein kann. Wenn Sie z. B. ein einfaches Rechteck zeichnen, ist der Wert der Zelle ObjType 0. Wenn Sie dann das **Verbindertool** verwenden, um das Rechteck mit einer anderen Form zu verbinden, setzt Visio den Wert der Zelle ObjType des Rechtecks auf 1 zurück (platzierbar). 
  
Der Wert der Zelle ObjType kann eine Kombination aus mehreren verschiedenen Werten sein. Wenn das nicht platzierbare Bit festgelegt ist ( &amp; H4), hat es jedoch Vorrang vor anderen Werten außer dem Gruppenwert ( &amp; H8).
  
Um einen Verweis auf die Zelle ObjType anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ObjType  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ObjType anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowMisc** <br/> |
|Zellenindex:  <br/> |**visLOFlags** <br/> |
   

