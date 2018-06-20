---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- Hookexcelwindow-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8965cc6b1e3d24001c42744f2ee7d447aa4c79b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790514"
---
# <a name="hookexcelwindow"></a>HookExcelWindow

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird **ExcelCursorProc** installiert, sodass sie vor dem Hauptfenster **WndProc**Microsoft Excel aufgerufen wird.
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parameter

 _hWndExcel_ (**BEHANDELN**)
  
Die wichtigsten Excel-Fenster behandeln.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Die Funktion gibt keinen Wert zurück.
  
## <a name="remarks"></a>Hinweise

Die Funktion erhält die Adresse des Excel **WndProc** durch Verwendung **GetWindowLong()**. Speichert diesen Wert in ein globales, die das **WndProc** aufrufen und auch wiederherstellen verwendet werden können. Schließlich wird diese Adresse mit der Adresse des **ExcelCursorProc** mit **SetWindowLong()** ersetzt.
  
### <a name="example"></a>Beispiel

Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

