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
ms.localizationpriority: medium
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 788afcb9a1ca04931f3cb74c5c3b3fe5805541c3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596862"
---
# <a name="unhookexcelwindow"></a>UnhookExcelWindow

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Entfernt den **ExcelCursorProc,** der zuvor von **HookExcelWindow** installiert wurde. Dies wäre so geschehen, dass **ExcelCursorProc** vor dem Microsoft Excel **WndProc-Hauptmodul** aufgerufen wurde.
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parameter

 _hWndExcel_ (**HANDLE**)
  
Der Excel Haupthandle Windows.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion gibt keinen Wert zurück.
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Funktion stellt die Excel **Standard-WndProc** mithilfe von **SetWindowLong()** wieder her, um die Adresse wiederherzustellen, die von **HookExcelWindow()** gespeichert wurde.
  
### <a name="example"></a>Beispiel

Informationen zum Quellcode für diese Funktion finden Sie  `\SAMPLES\GENERIC\GENERIC.C` unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

