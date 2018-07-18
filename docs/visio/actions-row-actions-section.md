---
title: Zeile "Actions" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60017
localization_priority: Normal
ms.assetid: 29a7464a-b9d4-a8ea-161b-3044de32ed23
description: Enthält Zellen, die einen benutzerdefinierten Befehl in einem Kontext- oder Aktionstagmenü zugeordneten Aktionen angeben. Abschnitt "Actions" enthält eine Zeile von Aktionen für die einzelnen Aktionen.
ms.openlocfilehash: f25ab75fe2bec35b09d2910ef731d11264224b7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796383"
---
# <a name="actions-row-actions-section"></a>Zeile "Actions" (Abschnitt "Actions")

Enthält Zellen, die einen benutzerdefinierten Befehl in einem Kontext- oder Aktionstagmenü zugeordneten Aktionen angeben. Abschnitt "Actions" enthält eine Zeile von Aktionen für die einzelnen Aktionen.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
Aktionszeilen heißen Aktionen. *Name* und enthält folgenden Zellen. Weitere Informationen finden Sie unter die folgenden Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[Action](action-cell-actions-section.md) <br/> |Enthält die Formel, die ausgeführt werden soll, wenn ein Benutzer ein Element in einem Kontext- oder Aktionstagmenü auswählt.
  <br/> |
|[Menü](menu-cell-actions-section.md) <br/> |Definiert den Namen des Menüelements, das angezeigt wird in einem Aktionstag- oder Kontextmenü.  <br/> |
|[TagName](tagname-cell-actions-section.md) <br/> |Der logische Name des Aktionstags, in dem diese Aktion erfolgen soll.  <br/> |
|[ButtonFace](buttonface-cell-actions-section.md) <br/> |Bestimmt das Symbol, das neben einem Element in einem Kontext- oder Aktionstagmenü angezeigt wird.  <br/> |
|[SortKey](sortkey-cell-actions-section.md) <br/> |Eine Zahl, die die Reihenfolge der Menüelemente in einem Aktionstag- oder Kontextmenü bestimmt.  <br/> |
|[Checked](checked-cell-actions-section.md) <br/> |Gibt an, ob das Menüelement in einem Aktionstag- oder Kontextmenü aktiviert ist.  <br/> |
|[Deaktiviert](disabled-cell-actions-section.md) <br/> |Gibt an, ob ein Menüelement in einem Kontext- oder Aktionstagmenü deaktiviert ist.  <br/> |
|[ReadOnly](readonly-cell-actions-section.md) <br/> |Gibt an, ob das Menüelement schreibgeschützt ist (es kann nicht darauf geklickt werden).  <br/> |
|[Nicht sichtbare](invisible-cell-actions-section.md) <br/> |Zeigt an, ob das Menüelement in einem Aktionstag- oder Kontextmenü sichtbar ist.  <br/> |
|[BeginGroup](begingroup-cell-actions-section.md) <br/> |Gibt an, ob im Menü über das Menüelement ein Trennzeichen einzufügen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 Sie können so viele Aktionen hinzufügen.  *Namen* Zeilen wie Sie benötigen, den Zeilen aussagekräftige Namen zuweisen und Zellenwerte festlegen. Klicken Sie zum Hinzufügen eines benutzerdefinierten Befehls zu einem vorhandenen Abschnitt Actions Maustaste auf eine Zeile, und klicken Sie im Kontextmenü auf **Zeile einfügen** . 
  
Sie können diese Zellen anhand ihrer Zeilennamen verweisen, die in einem ShapeSheet-Fenster als roter Text angezeigt. Ein Aktionen einen aussagekräftigen Namen zuweisen. Zeile *Name* , klicken Sie auf die Zeile, und geben Sie einen Namen wie beispielsweise *benutzerdefinierte* , beispielsweise zum Erstellen der Zeile mit dem Namen Actions.Custom zu definieren. Sie können dann die Zelle Menu verweisen, mithilfe von Actions.Custom.Menu. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

