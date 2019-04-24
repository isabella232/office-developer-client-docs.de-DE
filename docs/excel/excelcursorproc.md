---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- excelcursorproc-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d3cc41487f0cae31e110249fe148f5370319a39a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304095"
---
# <a name="excelcursorproc"></a>ExcelCursorProc

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wenn ein modales Dialogfeld über das Microsoft Excel-Fenster angezeigt wird, ist der Cursor ein Beschäftigter Cursor über das Excel-Fenster. Dieser **WndProc** -Traps WM_SETCURSOR Windows-Meldungen und ändert den Cursor zurück zu einem normalen Pfeil. 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Parameter

 _hWndDlg_ (**HWND**)
  
Enthält das HWND-Windows-Handle des Dialogfelds.
  
 _Nachricht_ (**Uint**)
  
Die Nachricht, auf die geantwortet werden soll.
  
 _wParam_ (**WParam**)
  
 _LPARAM_ (**LPARAM**)
  
Von Windows übergebene Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

LRESULT: 0, wenn die Nachricht behandelt wurde, andernfalls das von der Standard- **WndProc**-Objekt zurückgegebene Ergebnis.
  
### <a name="example"></a>Beispiel

Den `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

