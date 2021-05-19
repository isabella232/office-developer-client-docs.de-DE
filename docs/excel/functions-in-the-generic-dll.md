---
title: Funktionen in allgemeinen DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- generic dll [excel 2007], functions,functions [Excel 2007], Generic DLL
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3064e1a09ad8850e121da678f3702a6236574599
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420598"
---
# <a name="functions-in-the-generic-dll"></a>Funktionen in allgemeinen DLL

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Der Ordner enthält Microsoft Visual Studio Projektdateien und Quellcodedateien, die zum `\EXAMPLES\GENERIC\` Kompilieren der Beispiel-DLL GENERIC.xll erforderlich sind. Sie können dieses Projekt als Vorlage zum Schreiben eigener xlLs Microsoft Excel verwenden. Der Quellcode in diesem Projekt veranschaulicht viele der Features der Excel C-API. 
  
Beim Laden von GENERIC.xll wird ein neues Menü **"Generic"** mit vier Befehlen erstellt: 
  
- **Dialogfeld** – Zeigt ein Microsoft Excel an. 
    
- **Tanz** – Verschiebt die Auswahl, bis Sie die **ESC-TASTE** drücken. 
    
- **Systemeigenes** Dialogfeld – Zeigt ein Windows dialogfeld an. 
    
- **Exit** – Entladen Sie GENERIC.xll und entfernt das Menü **Generisch.** 
    
GENERIC.xll bietet außerdem drei Arbeitsblattfunktionen, Func1, FuncSum und FuncFib, die verwendet werden können, wenn GENERIC.xll geladen wird. GENERIC.xll kann mit dem Add-In-Manager geladen werden, oder es wird geladen, wenn es am normalen Ende der letzten Sitzung aktiv Excel war.
  
Dieses Projekt verwendet die Framework library (FRMWRK32.lib).
  
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

