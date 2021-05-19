---
title: Anzeigen von Dialogfelder aus einer DLL oder XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlls [excel 2007], Anzeigen von Dialogfelder aus,Dialogfelder [Excel 2007], Anzeigen aus einer DLL oder XLL,DLLs [Excel 2007], Anzeigen von Dialogfelder aus
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7b00430b047fe792afef701d210ccde06dd16216
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417868"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>Anzeigen von Dialogfelder aus einer DLL oder XLL

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Um ein Win32-Dialogfeld mit z. B. der Windows SDK-Funktion **DialogBox** anzuzeigen, müssen Sie zuerst die vollständige 32-Bit-Instanz und die Hauptfensterziehpunkte für Excel abrufen. Weitere Informationen finden Sie unter [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md). 
  
Wenn Ihr Projekt die Dialogfeldressource enthält, müssen Sie mehrere Schritte ausführen, um die Nachrichtenbehandlungsroutine auf die des neu angezeigten Dialogfelds zu setzen und die Excel-Nachrichtenbehandlungsroutine wiederherzustellen, wenn das Dialogfeld geschlossen wird. Der Beispielbefehl [fShowDialog](fshowdialog.md) im Generic-Projekt veranschaulicht die Verwendung der Windows-Funktionen, um dies ordnungsgemäß auszuführen. 
  
Sie können auch Dialogfelder mit der C-API anzeigen, ohne Windows SDK-Funktionen verwenden zu müssen. Die Dialogfeldfunktionen der C-API sind jedoch im Vergleich zu Windows, Visual Basic for Applications (VBA) oder Microsoft Foundation Classes (MFC) sehr eingeschränkt. (Beispielsweise sind C-API-Dialogfelder immer modal).
  
## <a name="see-also"></a>Siehe auch



[Erstellen von XLLs](creating-xlls.md)
  
[Entwickeln von DLLs](developing-dlls.md)
  
[Zugreifen auf Excel-Instanz- und Hauptfensterhandles](how-to-access-excel-instance-and-main-window-handles.md)
  
[C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

