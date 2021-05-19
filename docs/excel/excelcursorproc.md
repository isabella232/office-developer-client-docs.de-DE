---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- excelcursorproc-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d3cc41487f0cae31e110249fe148f5370319a39a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432492"
---
# <a name="excelcursorproc"></a>ExcelCursorProc

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wenn ein modales Dialogfeld über dem Fenster Microsoft Excel angezeigt wird, ist der Cursor ein beschäftigter Cursor über Excel Fenster. Dieses **WndProc-Traping** WM_SETCURSOR Typ Windows Nachrichten und ändert den Cursor zurück in einen normalen Pfeil. 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Parameter

 _hWndDlg_ (**HWND**)
  
Enthält das HWND-Windows-Handle des Dialogfelds.
  
 _message_ (**UINT**)
  
Die Nachricht, auf die reagiert werden soll.
  
 _wParam_ (**WPARAM**)
  
 _lParam_ (**LPARAM**)
  
Argumente, die von Windows.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

LRESULT: 0, wenn die Nachricht verarbeitet wurde, andernfalls das Vom **Standard-WndProc zurückgegebene Ergebnis.**
  
### <a name="example"></a>Beispiel

Den  `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

