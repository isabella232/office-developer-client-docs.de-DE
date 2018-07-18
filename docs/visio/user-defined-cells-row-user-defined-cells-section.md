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
ms.openlocfilehash: 45a9a033fe486a14e9881c3d79b79a129ecedc1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798354"
---
# <a name="user-defined-cells-row-user-defined-cells-section"></a>Zeile "User-defined Cells" (Abschnitt "User-defined Cells")

Enthält den Wert und die beschreibende Eingabeaufforderung für jede benutzerdefinierte Zelle in Ihrer Lösung. Ein Shape enthält für jedes Paar von Zellen mit Wert und Eingabeaufforderung eine User-defined Cells-Zeile.
  
Zeilen User-defined Cells heißen Benutzer. *Name* und enthält folgenden Zellen. Weitere Informationen finden Sie unter die folgenden Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[Value](value-cell-user-defined-cells-section.md) <br/> |Gibt einen Wert für die entsprechende benutzerdefinierte Zelle an.  <br/> |
|[Prompt](prompt-cell-user-defined-cells-section.md) <br/> |Gibt eine beschreibende Eingabeaufforderung bzw. einen Kommentar für die benutzerdefinierte Zelle an.  <br/> |
   
## <a name="remarks"></a>Hinweise

Benutzerdefinierte Zellen können für die Eingabe von Formeln oder Konstanten verwendet werden, auf die durch andere Zellen oder Add-Ons verwiesen wird. Werte in benutzerdefinierten Zellen sind portabel. Wenn ein Shape, das auf eine benutzerdefinierte Zelle in einem Shape verweist, in ein anderes Shape kopiert wird, das nicht dieselbe benutzerdefinierte Zelle enthält, wird die Zelle dem Shape hinzugefügt.
  
 Sie können beliebig viele Benutzer hinzufügen.  *Namen* Zeilen wie Sie benötigen, den Zeilen aussagekräftige Namen zuweisen und Zellenwerte festlegen. Um eine Zeile eines vorhandenen Abschnitts User-defined Cells hinzuzufügen, mit der rechten Maustaste in einer Zeile, und klicken Sie im Kontextmenü auf **Zeile einfügen** . 
  
Sie können diese Zellen anhand ihrer Zeilennamen verweisen, die in einem ShapeSheet-Fenster als roter Text angezeigt. Um Benutzer aussagekräftige Namen zuzuweisen. *Namen* Zeilen, klicken Sie auf die Zeile, und geben Sie einen Namen wie beispielsweise *Offset* , beispielsweise, um die Zeile mit dem Namen User.Offset zu erstellen. Sie können dann die Zelle Prompt mit PROMT verweisen. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

