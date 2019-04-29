---
title: Zeile "User-defined Cells" (Abschnitt "User-defined Cells")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3060
localization_priority: Normal
ms.assetid: 6c48b9b3-5c62-7d5a-1c8f-fe96606f4dea
description: Enthält den Wert und die beschreibende Eingabeaufforderung für jede benutzerdefinierte Zelle in Ihrer Lösung. Ein Shape enthält für jedes Paar von Zellen mit Wert und Eingabeaufforderung eine User-defined Cells-Zeile.
ms.openlocfilehash: 01e2da8ef1e97e8a911df605ab6cf1e9f8a853eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420689"
---
# <a name="user-defined-cells-row-user-defined-cells-section"></a>Zeile "User-defined Cells" (Abschnitt "User-defined Cells")

Enthält den Wert und die beschreibende Eingabeaufforderung für jede benutzerdefinierte Zelle in Ihrer Lösung. Ein Shape enthält für jedes Paar von Zellen mit Wert und Eingabeaufforderung eine User-defined Cells-Zeile.
  
Benutzerdefinierte Zellen Zeilen werden als Benutzer bezeichnet. *Name* und enthalten die folgenden Zellen. Weitere Informationen finden Sie in den Themen zu bestimmten Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[Wert](value-cell-user-defined-cells-section.md) <br/> |Gibt einen Wert für die entsprechende benutzerdefinierte Zelle an.  <br/> |
|[Prompt](prompt-cell-user-defined-cells-section.md) <br/> |Gibt eine beschreibende Eingabeaufforderung bzw. einen Kommentar für die benutzerdefinierte Zelle an.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Benutzerdefinierte Zellen können für die Eingabe von Formeln oder Konstanten verwendet werden, auf die durch andere Zellen oder Add-Ons verwiesen wird. Werte in benutzerdefinierten Zellen sind portabel. Wenn ein Shape, das auf eine benutzerdefinierte Zelle in einem Shape verweist, in ein anderes Shape kopiert wird, das nicht dieselbe benutzerdefinierte Zelle enthält, wird die Zelle dem Shape hinzugefügt.
  
 Sie können so viele Benutzer hinzufügen.  *benennen* Sie Zeilen, die Sie benötigen, und weisen Sie den Zeilen aussagekräftige Namen zu. Um einer vorhandenen benutzerdefinierten Zelle eine Zeile hinzuzufügen, klicken Sie mit der rechten Maustaste auf eine Zeile, und klicken Sie dann im Kontextmenü auf **Zeile einfügen** . 
  
Sie können auf diese Zellen anhand ihres Zeilennamens verweisen, der in einem ShapeSheet-Fenster in rotem Text angezeigt wird. Dem Benutzer aussagekräftige Namen zuweisen. *Name* rows, klicken Sie auf die Zeile, und geben Sie dann einen Namen wie *Offset* ein, um beispielsweise den Zeilennamen User. Offset zu erstellen. Sie können dann mithilfe von User. Offset. reansage auf die Zelle "Ansage" verweisen. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

