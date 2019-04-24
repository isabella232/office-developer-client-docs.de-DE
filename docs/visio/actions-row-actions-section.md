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
description: Enthält Zellen, die die Aktionen angeben, die einem benutzerdefinierten Befehl in einem Kontext-oder aktionstagmenü zugeordnet sind. Der Abschnitt Actions enthält pro Aktion eine Actions-Zeile.
ms.openlocfilehash: 37464e98b3e4f7d07b2ae4bd391b31ec009b6726
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283044"
---
# <a name="actions-row-actions-section"></a>Zeile "Actions" (Abschnitt "Actions")

Enthält Zellen, die die Aktionen angeben, die einem benutzerdefinierten Befehl in einem Kontext-oder aktionstagmenü zugeordnet sind. Der Abschnitt Actions enthält pro Aktion eine Actions-Zeile.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
Aktionszeilen sind benannte Aktionen. *Name* und enthalten die folgenden Zellen. Weitere Informationen finden Sie in den Themen zu bestimmten Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[Action](action-cell-actions-section.md) <br/> |Enthält die Formel, die ausgeführt werden soll, wenn ein Benutzer ein Element in einem Kontext- oder Aktionstagmenü auswählt.  <br/> |
|[Menü](menu-cell-actions-section.md) <br/> |Definiert den Namen des Menüelements, das in einem Aktionstag oder Kontextmenü angezeigt wird.  <br/> |
|[TagName](tagname-cell-actions-section.md) <br/> |Der logische Name des Aktionstags, in dem diese Aktion erfolgen soll.  <br/> |
|["ButtonFace](buttonface-cell-actions-section.md) <br/> |Bestimmt das Symbol, das neben einem Element in einem Kontext- oder Aktionstagmenü angezeigt wird.  <br/> |
|[SortKey](sortkey-cell-actions-section.md) <br/> |Eine Zahl, die die Reihenfolge der Menüelemente in einem Aktionstag- oder Kontextmenü bestimmt.  <br/> |
|[Checked](checked-cell-actions-section.md) <br/> |Gibt an, ob das Menüelement in einem Aktionstag oder Kontextmenü aktiviert ist.  <br/> |
|[Disabled](disabled-cell-actions-section.md) <br/> |Gibt an, ob ein Menüelement in einem Kontext- oder Aktionstagmenü deaktiviert ist.  <br/> |
|[ReadOnly](readonly-cell-actions-section.md) <br/> |Gibt an, ob das Menüelement schreibgeschützt ist (es kann nicht darauf geklickt werden).  <br/> |
|[Unsichtbar](invisible-cell-actions-section.md) <br/> |Zeigt an, ob das Menüelement in einem Aktionstag- oder Kontextmenü sichtbar ist.  <br/> |
|[BeginGroup](begingroup-cell-actions-section.md) <br/> |Gibt an, ob ein Trennzeichen in das Menü oberhalb des Menüelements eingefügt werden soll.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 Sie können so viele Aktionen hinzufügen.  *benennen* Sie Zeilen, die Sie benötigen, und weisen Sie den Zeilen aussagekräftige Namen zu. Klicken Sie zum Hinzufügen eines benutzerdefinierten Befehls zu einem vorhandenen Aktionsbereich mit der rechten Maustaste auf eine Zeile, und klicken Sie dann im Kontextmenü auf **Zeile einfügen** . 
  
Sie können auf diese Zellen anhand ihres Zeilennamens verweisen, der in einem ShapeSheet-Fenster in rotem Text angezeigt wird. So weisen Sie einer Aktion einen aussagekräftigen Namen zu. Zeile *Name* , klicken Sie auf die Zeile, und geben Sie dann einen Namen wie *Custom* ein, um beispielsweise den Zeilennamen Actions. Custom zu erstellen. Mithilfe von Actions. Custom. Menu können Sie dann auf die Zelle Menu verweisen. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

