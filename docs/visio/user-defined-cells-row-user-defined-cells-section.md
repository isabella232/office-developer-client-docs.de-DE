---
title: Zeile "User-defined Cells" (Abschnitt "User-defined Cells")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3060
ms.localizationpriority: medium
ms.assetid: 6c48b9b3-5c62-7d5a-1c8f-fe96606f4dea
description: Enthält den Wert und die beschreibende Eingabeaufforderung für jede benutzerdefinierte Zelle in Ihrer Lösung. Ein Shape enthält für jedes Paar von Zellen mit Wert und Eingabeaufforderung eine User-defined Cells-Zeile.
ms.openlocfilehash: fe6c51c2586d84996bdce94134df872fd42b91fa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553648"
---
# <a name="user-defined-cells-row-user-defined-cells-section"></a>Zeile "User-defined Cells" (Abschnitt "User-defined Cells")

Enthält den Wert und die beschreibende Eingabeaufforderung für jede benutzerdefinierte Zelle in Ihrer Lösung. Ein Shape enthält für jedes Paar von Zellen mit Wert und Eingabeaufforderung eine User-defined Cells-Zeile.
  
Benutzerdefinierte Zellenzeilen heißen "Benutzer". *die*  folgenden Zellen benennen und enthalten. Weitere Informationen finden Sie in den spezifischen Zellthemen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[Wert](value-cell-user-defined-cells-section.md) <br/> |Gibt einen Wert für die entsprechende benutzerdefinierte Zelle an.  <br/> |
|[Prompt](prompt-cell-user-defined-cells-section.md) <br/> |Gibt eine beschreibende Eingabeaufforderung bzw. einen Kommentar für die benutzerdefinierte Zelle an.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Benutzerdefinierte Zellen können für die Eingabe von Formeln oder Konstanten verwendet werden, auf die durch andere Zellen oder Add-Ons verwiesen wird. Werte in benutzerdefinierten Zellen sind portabel. Wenn ein Shape, das auf eine benutzerdefinierte Zelle in einem Shape verweist, in ein anderes Shape kopiert wird, das nicht dieselbe benutzerdefinierte Zelle enthält, wird die Zelle dem Shape hinzugefügt.
  
 Sie können so viele Benutzer hinzufügen.  *Benennen*  Sie Zeilen nach Bedarf, weisen Sie den Zeilen aussagekräftige Namen zu, und legen Sie Zellwerte fest. Wenn Sie einem vorhandenen Abschnitt "Benutzerdefinierte Zellen" eine Zeile hinzufügen möchten, klicken Sie mit der rechten Maustaste auf eine Zeile, und klicken Sie im Kontextmenü auf **"Zeile einfügen".** 
  
Sie können auf diese Zellen anhand ihres Zeilennamens verweisen, der in einem ShapeSheet-Fenster in rotem Text angezeigt wird. So weisen Sie dem Benutzer aussagekräftige Namen zu. *Zeilen benennen,*  auf die Zeile klicken und dann einen Namen wie  *z. B. Offset*  eingeben, um den Zeilennamen User.Offset zu erstellen. Anschließend können Sie mit user.Offset.Prompt auf die Zelle "Prompt" verweisen. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

