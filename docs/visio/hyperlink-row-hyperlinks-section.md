---
title: Zeile "Hyperlink" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3065
ms.localizationpriority: medium
ms.assetid: e3c7ae27-2e54-a174-4fb3-d16093faf759
description: Enthält die Informationen für einen einzelnen Hyperlink, der einem Shape zugeordnet ist. Ein Shape enthält für jeden Hyperlink eine Hyperlink-Zeile.
ms.openlocfilehash: cb6cdaffd6f606bf9831a1b7708b02d3f727e274
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628192"
---
# <a name="hyperlink-row-hyperlinks-section"></a>Zeile "Hyperlink" (Abschnitt "Hyperlinks")

Enthält die Informationen für einen einzelnen Hyperlink, der einem Shape zugeordnet ist. Ein Shape enthält für jeden Hyperlink eine Hyperlink-Zeile.
  
Hyperlinkzeilen heißen "Hyperlink". *die*  folgenden Zellen benennen und enthalten. Weitere Informationen finden Sie in den spezifischen Zellthemen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[Beschreibung](description-cell-hyperlinks-section.md) <br/> |Ein beschreibender Text als Zeichenfolge für einen Hyperlink.  <br/> |
|[Adresse](address-cell-hyperlinks-section.md) <br/> |URL-Adresse (Uniform Resource Locator), MS-DOS-Dateiname oder UNC-Pfad (Universal Naming Convention), zu der bzw. zu dem gewechselt werden soll.  <br/> |
|[SubAddress](subaddress-cell-hyperlinks-section.md) <br/> |Eine Stelle im Zieldokument für die Verknüpfung.  <br/> |
|[ExtraInfo](extrainfo-cell-hyperlinks-section.md) <br/> |Eine Zeichenfolge, die Informationen für die Auflösung der URL übergibt.  <br/> |
|[Frame](frame-cell-hyperlinks-section.md) <br/> |Der Name eines Rahmens, der als Ziel dienen soll, wenn Microsoft Office Visio als ActiveX-Dokument in einem ActiveX-Container geöffnet ist. Der Standardwert ist eine leere Zeichenfolge.  <br/> |
|[Sortkey](sortkey-cell-hyperlinks-section.md) <br/> |Bestimmt die Reihenfolge der Hyperlinks, in der sie im Kontextmenü angezeigt werden.  <br/> |
|[NewWindow](newwindow-cell-hyperlinks-section.md) <br/> |Gibt an, ob der Hyperlink in einem neuen Fenster geöffnet werden soll. Bei TRUE wird die verknüpfte Seite, das verknüpfte Dokument oder die verknüpfte Website in einem neuen Fenster geöffnet. Die Standardeinstellung ist FALSE.  <br/> |
|[Default](default-cell-hyperlinks-section.md) <br/> |Der Standardhyperlink für ein Shape oder ein Zeichenblatt.  <br/> |
|[Unsichtbar](invisible-cell-hyperlinks-section.md) <br/> |Gibt an, ob der Hyperlink im Kontextmenü angezeigt wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 Sie können so viele Hyperlinks hinzufügen.  *Benennen*  Sie Zeilen nach Bedarf, weisen Sie den Zeilen aussagekräftige Namen zu, und legen Sie Zellwerte fest. Klicken Sie mit der rechten Maustaste auf eine Zeile, und klicken Sie im Kontextmenü auf **"Zeile einfügen",** um einem vorhandenen Abschnitt "Hyperlinks" Hyperlinks hinzuzufügen. 
  
Sie können auf diese Zellen anhand ihres Zeilennamens verweisen, der in einem ShapeSheet-Fenster in rotem Text angezeigt wird. So weisen Sie Hyperlink aussagekräftige Namen zu. *Benennen*  Sie Zeilen, klicken Sie auf die Zeile, und geben Sie dann einen Namen wie z.  *B. Marketing*  ein, um den Zeilennamen Hyperlink.Marketing zu erstellen. Anschließend können Sie mithilfe von Hyperlink.Marketing.Description auf die Zelle Description verweisen. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

