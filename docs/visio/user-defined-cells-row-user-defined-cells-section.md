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
  
Benutzerdefinierte Zellenzeilen heißen User. *namen*  und die folgenden Zellen enthalten. Weitere Informationen finden Sie in den spezifischen Zellthemen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[Wert](value-cell-user-defined-cells-section.md) <br/> |Gibt einen Wert für die entsprechende benutzerdefinierte Zelle an.  <br/> |
|[Prompt](prompt-cell-user-defined-cells-section.md) <br/> |Gibt eine beschreibende Eingabeaufforderung bzw. einen Kommentar für die benutzerdefinierte Zelle an.  <br/> |
   
## <a name="remarks"></a>Hinweise

Benutzerdefinierte Zellen können für die Eingabe von Formeln oder Konstanten verwendet werden, auf die durch andere Zellen oder Add-Ons verwiesen wird. Werte in benutzerdefinierten Zellen sind portabel. Wenn ein Shape, das auf eine benutzerdefinierte Zelle in einem Shape verweist, in ein anderes Shape kopiert wird, das nicht dieselbe benutzerdefinierte Zelle enthält, wird die Zelle dem Shape hinzugefügt.
  
 Sie können so viele Benutzer hinzufügen.  *name*  rows as you need, assign meaningful names to the rows, and set cell values. Klicken Sie zum Hinzufügen einer Zeile zu einem vorhandenen Abschnitt Benutzerdefinierte Zellen mit der rechten Maustaste auf eine Zeile, und klicken Sie im Kontextmenü **auf** Zeile einfügen. 
  
Sie können auf diese Zellen durch ihren Zeilennamen verweisen, der in einem ShapeSheet-Fenster in rotem Text angezeigt wird. So weisen Sie dem Benutzer aussagekräftige Namen zu. *Zeilen*  benennen, klicken Sie auf die Zeile, und geben Sie dann einen Namen wie  *Offset*  ein, z. B. zum Erstellen des Zeilennamens User.Offset. Anschließend können Sie mithilfe von User.Offset.Prompt auf die Zelle Eingabeaufforderung verweisen. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

