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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355825"
---
# <a name="viewmarkup-cell-document-properties-section"></a>Zelle "ViewMarkup" (Abschnitt "Document Properties")

Bestimmt, ob im Zeichnungsfenster Markup angezeigt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Markup wird in der Zeichnung angezeigt.  <br/> |
|FALSE  <br/> |Markup wird nicht angezeigt (Standardwert).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 Wenn die Markupverfolgung aktiviert ist (die addMarkup-Zelle ist TRUE), wird die Zelle "ViewMarkup automatisch auf TRUE festgelegt und bleibt auch dann TRUE, wenn die Markupverfolgung deaktiviert ist (addMarkup cell is FALSE). Der Wert in der Zelle ViewMarkup wird ignoriert, wenn die Zelle AddMarkup WAHR ist. 
  
Die Zelle ViewMarkup wird ebenfalls auf WAHR festgelegt, wenn Kommentare in eine Zeichnung eingefügt werden (wobei es keine Rolle spielt, ob die Markupverfolgung aktiviert ist oder nicht) und muss auf WAHR festgelegt sein, damit die Kommentare in der Zeichnung sichtbar sind.
  
Diese Zelle entspricht dem Befehl **Markup anzeigen** in der Gruppe **Markup** der Registerkarte **Überprüfen**. 
  
Wenn Sie einen Verweis auf die Zelle "ViewMarkup aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |"ViewMarkup  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "ViewMarkup aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowDoc** <br/> |
|Zellenindex:  <br/> |**visDocViewMarkup** <br/> |
   

