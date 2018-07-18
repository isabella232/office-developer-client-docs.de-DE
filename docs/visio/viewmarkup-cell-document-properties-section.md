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
ms.openlocfilehash: dda908595b243878ec755cf73351ec1fd672dc55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798403"
---
# <a name="viewmarkup-cell-document-properties-section"></a>ViewMarkup Cell (Document Properties Section)

Bestimmt, ob im Zeichnungsfenster Markup angezeigt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|WAHR  <br/> |Markup wird in der Zeichnung angezeigt.  <br/> |
|FALSCH  <br/> |Markup wird nicht angezeigt (Standardwert).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 Wenn Markup verfolgen aktiviert ist (die Zelle AddMarkup ist TRUE), die Zelle ViewMarkup automatisch auf TRUE festgelegt ist und der Wert WAHR auch nach dem Markup verfolgen deaktiviert ist (die Zelle AddMarkup ist FALSE). Der Wert in der Zelle ViewMarkup wird ignoriert, wenn die Zelle AddMarkup auf true festgelegt ist. 
  
Die Zelle ViewMarkup wird ebenfalls auf WAHR festgelegt, wenn Kommentare in eine Zeichnung eingefügt werden (wobei es keine Rolle spielt, ob die Markupverfolgung aktiviert ist oder nicht) und muss auf WAHR festgelegt sein, damit die Kommentare in der Zeichnung sichtbar sind.
  
Diese Zelle entspricht dem Befehl **Markup anzeigen** in der Gruppe **Markup** der Registerkarte **Überprüfen**. 
  
Wenn Sie einen Verweis auf die Zelle ViewMarkup aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ViewMarkup  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ViewMarkup aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowDoc** <br/> |
|Zellenindex:  <br/> |**visDocViewMarkup** <br/> |
   

