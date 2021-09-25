---
title: Zeile "Actions" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60017
ms.localizationpriority: medium
ms.assetid: 29a7464a-b9d4-a8ea-161b-3044de32ed23
description: Enthält Zellen, die die Aktionen angeben, die einem benutzerdefinierten Befehl in einem Kontext- oder Aktionstagmenü zugeordnet sind. Der Abschnitt Actions enthält pro Aktion eine Actions-Zeile.
ms.openlocfilehash: 21b0fe801b7041f7de9a7b4dfcd559e8ea553356
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616131"
---
# <a name="actions-row-actions-section"></a>Zeile "Actions" (Abschnitt "Actions")

Enthält Zellen, die die Aktionen angeben, die einem benutzerdefinierten Befehl in einem Kontext- oder Aktionstagmenü zugeordnet sind. Der Abschnitt Actions enthält pro Aktion eine Actions-Zeile.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
Aktionszeilen heißen "Aktionen". *die*  folgenden Zellen benennen und enthalten. Weitere Informationen finden Sie in den spezifischen Zellthemen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[Action](action-cell-actions-section.md) <br/> |Enthält die Formel, die ausgeführt werden soll, wenn ein Benutzer ein Element in einem Kontext- oder Aktionstagmenü auswählt.  <br/> |
|[Menü](menu-cell-actions-section.md) <br/> |Definiert den Namen des Menüelements, das in einem Aktionstag oder Kontextmenü angezeigt wird.  <br/> |
|[Tagname](tagname-cell-actions-section.md) <br/> |Der logische Name des Aktionstags, in dem diese Aktion erfolgen soll.  <br/> |
|[ButtonFace](buttonface-cell-actions-section.md) <br/> |Bestimmt das Symbol, das neben einem Element in einem Kontext- oder Aktionstagmenü angezeigt wird.  <br/> |
|[Sortkey](sortkey-cell-actions-section.md) <br/> |Eine Zahl, die die Reihenfolge der Menüelemente in einem Aktionstag- oder Kontextmenü bestimmt.  <br/> |
|[Checked](checked-cell-actions-section.md) <br/> |Gibt an, ob das Menüelement in einem Aktionstag- oder Kontextmenü aktiviert ist.  <br/> |
|[Disabled](disabled-cell-actions-section.md) <br/> |Gibt an, ob ein Menüelement in einem Kontext- oder Aktionstagmenü deaktiviert ist.  <br/> |
|[ReadOnly](readonly-cell-actions-section.md) <br/> |Gibt an, ob das Menüelement schreibgeschützt ist (es kann nicht darauf geklickt werden).  <br/> |
|[Unsichtbar](invisible-cell-actions-section.md) <br/> |Zeigt an, ob das Menüelement in einem Aktionstag- oder Kontextmenü sichtbar ist.  <br/> |
|[BeginGroup](begingroup-cell-actions-section.md) <br/> |Gibt an, ob oberhalb des Menüelements ein Trennzeichen in das Menü eingefügt werden soll.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 Sie können so viele Aktionen hinzufügen.  *Benennen*  Sie Zeilen nach Bedarf, weisen Sie den Zeilen aussagekräftige Namen zu, und legen Sie Zellwerte fest. Um einem vorhandenen Abschnitt "Aktionen" einen benutzerdefinierten Befehl hinzuzufügen, klicken Sie mit der rechten Maustaste auf eine Zeile, und klicken Sie im Kontextmenü auf **"Zeile einfügen".** 
  
Sie können auf diese Zellen anhand ihres Zeilennamens verweisen, der in einem ShapeSheet-Fenster in rotem Text angezeigt wird. So weisen Sie einem Actions-Objekt einen aussagekräftigen Namen zu. *name*  row, click the row, and then type a name such as  *Custom*  , for example, to create the row name Actions.Custom. Anschließend können Sie mithilfe von Actions.Custom.Menu auf die Zelle Menu verweisen. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

