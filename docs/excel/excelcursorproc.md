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
ms.localizationpriority: medium
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 621a03c00ee4d1509edd3dd8b14a11dba9ba719a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584927"
---
# <a name="excelcursorproc"></a>ExcelCursorProc

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wenn über dem Microsoft Excel Fenster ein modales Dialogfeld angezeigt wird, ist der Cursor ein beschäftigter Cursor über dem Excel Fenster. Mit diesem **WndProc** wird WM_SETCURSOR Typ Windows Nachrichten auffangen und der Cursor wieder in einen normalen Pfeil geändert. 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Parameter

 _hWndDlg_ (**HWND**)
  
Enthält das HWND-Windows Handle des Dialogfelds.
  
 _message_ (**UINT**)
  
Die Nachricht, auf die reagiert werden soll.
  
 _wParam_ (**WPARAM**)
  
 _lParam_ (**LPARAM**)
  
Von Windows übergebene Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

LRESULT: 0, wenn die Nachricht verarbeitet wurde, andernfalls das Ergebnis, das von der **Standard-WndProc** zurückgegeben wird.
  
### <a name="example"></a>Beispiel

Informationen zum Quellcode für diese Funktion finden Sie  `\SAMPLES\GENERIC\GENERIC.C` unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

