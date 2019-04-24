---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- unhookexcelwindow-Funktion
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: aef2734aeb4d9cf5df33e3d012cef309e8a1eb6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310311"
---
# <a name="unhookexcelwindow"></a>UnhookExcelWindow

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Entfernt die **ExcelCursorProc** , die zuvor von **HookExcelWindow**installiert wurde. Dies wäre getan worden, damit **ExcelCursorProc** vor dem Haupt- **WndProc**von Microsoft Excel aufgerufen wurde.
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parameter

 _hWndExcel_ (**Handle**)
  
Der Excel-Hauptfenster-handle.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion gibt keinen Wert zurück.
  
## <a name="remarks"></a>Bemerkungen

Diese Funktion stellt die Excel-Standard- **WndProc** mithilfe von **SetWindowLong ()** wieder her, um die von **HookExcelWindow ()** gespeicherte Adresse wiederherzustellen.
  
### <a name="example"></a>Beispiel

Den `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

