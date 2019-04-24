---
title: Funktionen in allgemeinen DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- generische dll [Excel 2007], Funktionen, Funktionen [Excel 2007], generische DLL
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3064e1a09ad8850e121da678f3702a6236574599
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304088"
---
# <a name="functions-in-the-generic-dll"></a>Funktionen in allgemeinen DLL

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Der Ordner `\EXAMPLES\GENERIC\` enthält Microsoft Visual Studio-Projektdateien und Quellcodedateien, die zum Kompilieren der Beispiel-dll Generic. XLL benötigt werden. Sie können dieses Projekt als Vorlage zum Schreiben eigener Microsoft Excel-XLLs verwenden. Der Quellcode in diesem Projekt demonstriert viele der Features der Excel C-API. 
  
Wenn Sie generische. XLL laden, wird ein neues **generisches** Menü mit vier Befehlen erstellt: 
  
- **Dialog** -zeigt ein Microsoft Excel-Dialogfeld an. 
    
- **Dance** -verschiebt die Auswahl um, bis Sie die **ESC** -Taste drücken. 
    
- **Native Dialog** – zeigt ein Windows-Dialogfeld an. 
    
- **Exit** -entlädt generische. XLL und entfernt das **generische** Menü. 
    
GENERISCHE. XLL stellt auch drei Arbeitsblattfunktionen, func1, FuncSum und FuncFib, die verwendet werden können, wenn generische. XLL geladen wird. GENERISCHE. XLL kann mit dem Add-in-Manager geladen werden, oder Sie wird geladen, wenn Sie am normalen Ende der letzten Excel-Sitzung aktiv war.
  
Dieses Projekt verwendet die Framework-Bibliothek (FRMWRK32. lib).
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[DIALOGMsgProc](dialogmsgproc.md)
  
[ExcelCursorProc](excelcursorproc.md)
  
[HookExcelWindow](hookexcelwindow.md)
  
[UnhookExcelWindow](unhookexcelwindow.md)
  
[fShowDialog](fshowdialog.md)
  
[fDance](fdance.md)
  
[fDialog/fDialog12](fdialog-fdialog12.md)
  
[fExit](fexit.md)
  
[Func1](func1.md)
  
[FuncSum](funcsum.md)
  
[FuncFib](funcfib.md)
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

