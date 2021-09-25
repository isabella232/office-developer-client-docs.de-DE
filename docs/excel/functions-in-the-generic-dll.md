---
title: Funktionen in allgemeinen DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- generic dll [excel 2007], functions,functions [Excel 2007], Generic DLL
ms.localizationpriority: medium
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: dcbbf753c5029f92b2445233a454233ad3fa8f32
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617202"
---
# <a name="functions-in-the-generic-dll"></a>Funktionen in allgemeinen DLL

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Der Ordner `\EXAMPLES\GENERIC\` enthält Microsoft Visual Studio Projektdateien und Quellcodedateien, die zum Kompilieren des Beispiels DLL GENERIC.xll erforderlich sind. Sie können dieses Projekt als Vorlage zum Schreiben eigener Microsoft Excel XLLs verwenden. Der Quellcode in diesem Projekt veranschaulicht viele der Features der Excel C-API. 
  
Wenn Sie GENERIC.xll laden, wird ein neues **generisches** Menü mit vier Befehlen erstellt: 
  
- **Dialogfeld** : Zeigt ein Microsoft Excel Dialogfeld an. 
    
-  Wiege – Verschiebt die Auswahl, bis Sie die **ESC-Taste** drücken. 
    
- **Systemeigenes Dialogfeld** – Zeigt ein Windows Dialogfeld an. 
    
- **Beenden –** Entlädt GENERIC.xll und entfernt das Menü **"Generisch".** 
    
GENERIC.xll bietet außerdem drei Arbeitsblattfunktionen, Func1, FuncSum und FuncFib, die verwendet werden können, wenn GENERIC.xll geladen wird. GENERIC.xll kann mit dem Add-In-Manager geladen werden, oder es wird geladen, wenn es am normalen Ende der letzten Excel Sitzung aktiv war.
  
Dieses Projekt verwendet die Frameworkbibliothek (FRMWRK32.lib).
  
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

