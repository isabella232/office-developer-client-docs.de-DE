---
title: Zelle "ViewMarkup" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
localization_priority: Normal
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: Bestimmt, ob im Zeichnungsfenster Markup angezeigt wird.
ms.openlocfilehash: eeccdd0d14bf28630937b0e480822abb6fb19da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416405"
---
# <a name="viewmarkup-cell-document-properties-section"></a>Zelle "ViewMarkup" (Abschnitt "Document Properties")

Bestimmt, ob im Zeichnungsfenster Markup angezeigt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Markup wird in der Zeichnung angezeigt.  <br/> |
|FALSE  <br/> |Markup wird nicht angezeigt (Standardwert).  <br/> |
   
## <a name="remarks"></a>Hinweise

 Wenn die Markupverfolgung aktiviert ist (Zelle AddMarkup ist TRUE), wird die Zelle ViewMarkup automatisch auf TRUE festgelegt und bleibt true, auch wenn die Markupverfolgung deaktiviert wurde (AddMarkup-Zelle ist FALSE). Der Wert in der Zelle ViewMarkup wird ignoriert, wenn die Zelle AddMarkup WAHR ist. 
  
Die Zelle ViewMarkup wird ebenfalls auf WAHR festgelegt, wenn Kommentare in eine Zeichnung eingefügt werden (wobei es keine Rolle spielt, ob die Markupverfolgung aktiviert ist oder nicht) und muss auf WAHR festgelegt sein, damit die Kommentare in der Zeichnung sichtbar sind.
  
Diese Zelle entspricht dem Befehl **Markup anzeigen** in der Gruppe **Markup** der Registerkarte **Überprüfen**. 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle ViewMarkup anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ViewMarkup  <br/> |
   
Um einen Verweis auf die Zelle ViewMarkup nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowDoc** <br/> |
|Zellenindex:  <br/> |**visDocViewMarkup** <br/> |
   

