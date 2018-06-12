---
title: Zeile "Hyperlink" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3065
localization_priority: Normal
ms.assetid: e3c7ae27-2e54-a174-4fb3-d16093faf759
description: Enthält die Informationen für einen einzelnen Hyperlink, der einem Shape zugeordnet ist. Ein Shape enthält für jeden Hyperlink eine Hyperlink-Zeile.
ms.openlocfilehash: 99295838f5d1860e3c34cf4e37866eb477fe81ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797173"
---
# <a name="hyperlink-row-hyperlinks-section"></a>Zeile "Hyperlink" (Abschnitt "Hyperlinks")

Enthält die Informationen für einen einzelnen Hyperlink, der einem Shape zugeordnet ist. Ein Shape enthält für jeden Hyperlink eine Hyperlink-Zeile.
  
Hyperlink Zeilen heißen Hyperlink. *Name* und enthält folgenden Zellen. Weitere Informationen finden Sie unter die folgenden Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[Description](description-cell-hyperlinks-section.md) <br/> |Ein beschreibender Text als Zeichenfolge für einen Hyperlink.  <br/> |
|[Address](address-cell-hyperlinks-section.md) <br/> |URL-Adresse (Uniform Resource Locator), MS-DOS-Dateiname oder UNC-Pfad (Universal Naming Convention), zu der bzw. zu dem gewechselt werden soll.  <br/> |
|[SubAddress](subaddress-cell-hyperlinks-section.md) <br/> |Eine Stelle im Zieldokument für die Verknüpfung.  <br/> |
|[ExtraInfo](extrainfo-cell-hyperlinks-section.md) <br/> |Eine Zeichenfolge, die Informationen für die Auflösung der URL übergibt.  <br/> |
|[Frame](frame-cell-hyperlinks-section.md) <br/> |Der Name eines Rahmens, der als Ziel dienen soll, wenn Microsoft Office Visio als ActiveX-Dokument in einem ActiveX-Container geöffnet ist. Der Standardwert ist eine leere Zeichenfolge.  <br/> |
|[SortKey](sortkey-cell-hyperlinks-section.md) <br/> |Bestimmt die Reihenfolge der Hyperlinks, in der sie im Kontextmenü angezeigt werden.  <br/> |
|[NewWindow](newwindow-cell-hyperlinks-section.md) <br/> |Gibt an, ob der Hyperlink in einem neuen Fenster geöffnet werden soll. Wenn dieser Wert auf TRUE festgelegt ist, wird das verknüpfte Zeichenblatt, das verknüpfte Dokument oder die verknüpfte Website in einem neuen Fenster geöffnet. Die Standardeinstellung ist FALSE.  <br/> |
|[Standard](default-cell-hyperlinks-section.md) <br/> |Der Standardhyperlink für ein Shape oder ein Zeichenblatt.  <br/> |
|[Nicht sichtbare](invisible-cell-hyperlinks-section.md) <br/> |Gibt an, ob der Hyperlink im Kontextmenü angezeigt wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

 Sie können beliebig viele Hyperlink hinzufügen.  *Namen* Zeilen wie Sie benötigen, den Zeilen aussagekräftige Namen zuweisen und Zellenwerte festlegen. Um einen vorhandenen Abschnitt Hyperlinks Hyperlinks hinzufügen, mit der rechten Maustaste in einer Zeile, und klicken Sie im Kontextmenü auf **Zeile einfügen** . 
  
Sie können diese Zellen anhand ihrer Zeilennamen verweisen, die in einem ShapeSheet-Fenster als roter Text angezeigt. Hyperlink aussagekräftige Namen zuzuweisen. *Namen* Zeilen, klicken Sie auf die Zeile, und geben Sie einen Namen wie *Marketing* , z. B., um die Zeile mit dem Namen Hyperlink.Marketing zu erstellen. Sie können dann auf die Zelle Description, indem Sie Hyperlink.Marketing.Description verwenden verweisen. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

