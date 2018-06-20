---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- Excelcursorproc-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 07be8da4a07b988d5e848048a088859b58ea3a14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790495"
---
# <a name="excelcursorproc"></a>ExcelCursorProc

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wenn ein modales Dialogfeld über das Microsoft Excel-Fenster angezeigt wird, ist der Cursor Mauszeiger über das Excel-Fenster. Diese **WndProc** Traps WM_SETCURSOR Geben Sie Windows-Nachrichten und ändert sich der Mauszeiger in einen normalen Pfeil sichern. 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>Parameter

 _hWndDlg_ (**HWND**)
  
Enthält das HWND Windows Handle des Dialogfelds.
  
 _Nachricht_ (**UINT**)
  
Die Nachricht zu antworten.
  
 _wParam_ (**WPARAM**)
  
 _lParam_ (**LPARAM**)
  
Durch Windows übergebene Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

LRESULT: 0, wenn die Meldung behandelt wurde, zurückgegeben, andernfalls das Ergebnis standardmäßig **WndProc**.
  
### <a name="example"></a>Beispiel

Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

