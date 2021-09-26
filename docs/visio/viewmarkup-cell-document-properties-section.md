---
title: Zelle "ViewMarkup" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
ms.localizationpriority: medium
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: Bestimmt, ob im Zeichnungsfenster Markup angezeigt wird.
ms.openlocfilehash: 29a4ec7b1d773e8f9d4fade27cf7d000d31a2c54
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597730"
---
# <a name="viewmarkup-cell-document-properties-section"></a>Zelle "ViewMarkup" (Abschnitt "Document Properties")

Bestimmt, ob im Zeichnungsfenster Markup angezeigt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Markup wird in der Zeichnung angezeigt.  <br/> |
|FALSE  <br/> |Markup wird nicht angezeigt (Standardwert).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

 Wenn die Markupverfolgung aktiviert ist (Zelle "AddMarkup" ist TRUE), wird die Zelle ViewMarkup automatisch auf TRUE festgelegt und bleibt true, auch wenn die Markupverfolgung deaktiviert wurde (Die Zelle AddMarkup ist FALSE). Der Wert in der Zelle ViewMarkup wird ignoriert, wenn die Zelle AddMarkup WAHR ist. 
  
Die Zelle ViewMarkup wird ebenfalls auf WAHR festgelegt, wenn Kommentare in eine Zeichnung eingefügt werden (wobei es keine Rolle spielt, ob die Markupverfolgung aktiviert ist oder nicht) und muss auf WAHR festgelegt sein, damit die Kommentare in der Zeichnung sichtbar sind.
  
Diese Zelle entspricht dem Befehl **Markup anzeigen** in der Gruppe **Markup** der Registerkarte **Überprüfen**. 
  
Um einen Verweis auf die Zelle ViewMarkup anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ViewMarkup  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ViewMarkup anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowDoc** <br/> |
|Zellenindex:  <br/> |**visDocViewMarkup** <br/> |
   

