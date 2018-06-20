---
title: Funktionen in der generische DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- generische Dll [excel 2007], Funktionen, Funktionen [Excel 2007], generische DLL
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e78f276e58ca1c98786e28ed5167762cf0bfdf7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790521"
---
# <a name="functions-in-the-generic-dll"></a>Funktionen in der generische DLL

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Der Ordner `\EXAMPLES\GENERIC\` enthält Microsoft Visual Studio-Projektdateien und Quellcodedateien, die erforderlich sind, um das Beispiel GENERIC.xll DLL zu kompilieren. Sie können dieses Projekt als Vorlage verwenden, für das Schreiben von eigenen Microsoft Excel-XLLs. Der Quellcode in diesem Projekt werden viele der Funktionen von Excel-C-API veranschaulicht. 
  
Wenn Sie GENERIC.xll laden, wird mit vier Befehle **generische** im Menü neues erstellt: 
  
- **Dialogfeld** - ein Microsoft Excel-Dialogfeld angezeigt. 
    
- **Tanz** - verschiebt die Auswahl um, bis Sie die **ESC** -Taste drücken. 
    
- **Systemeigene Dialogfeld** - ein Windows-Dialogfeld angezeigt. 
    
- **Exit** - entlädt GENERIC.xll, und klicken Sie im Menü **generische** entfernt. 
    
GENERIC.xll bietet auch drei Tabellenfunktionen, Func1, FuncSum und FuncFib, die verwendet werden kann, wenn GENERIC.xll geladen wird. GENERIC.xll können mit dem Add-In-Manager geladen werden, oder es wird geladen, wenn es am Ende der letzten Excel-Sitzung normalen aktiv war.
  
Dieses Projekt wird der Framework-Klassenbibliothek (FRMWRK32.lib) verwendet.
  
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

