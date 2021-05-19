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
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: aef2734aeb4d9cf5df33e3d012cef309e8a1eb6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409447"
---
# <a name="unhookexcelwindow"></a>UnhookExcelWindow

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Entfernt **excelCursorProc,** das zuvor von **HookExcelWindow installiert wurde.** Dies wäre so erfolgt, dass **ExcelCursorProc** vor dem Microsoft Excel **WndProc aufgerufen wurde.**
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parameter

 _hWndExcel_ (**HANDLE**)
  
Das Excel-Windows-Handle.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion gibt keinen Wert zurück.
  
## <a name="remarks"></a>Hinweise

Mit dieser Funktion wird die Excel **WndProc** mithilfe von **SetWindowLong()** wiederhergestellt, um die Adresse wiederherzustellen, die von **HookExcelWindow()** gespeichert wurde.
  
### <a name="example"></a>Beispiel

Den  `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

