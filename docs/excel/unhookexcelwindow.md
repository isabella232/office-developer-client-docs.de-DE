---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- Unhookexcelwindow-Funktion
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7b70bf4ed0ff45921df407605baa692c7621bca4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790582"
---
# <a name="unhookexcelwindow"></a>UnhookExcelWindow

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Entfernt die **ExcelCursorProc** , die zuvor durch **HookExcelWindow**installiert wurde. Dies würde ausgeführt werden, damit **ExcelCursorProc** vor der wichtigsten **WndProc**von Microsoft Excel aufgerufen wurde.
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parameter

 _hWndExcel_ (**BEHANDELN**)
  
Die wichtigsten Excel-Fenster behandeln.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Die Funktion gibt keinen Wert zurück.
  
## <a name="remarks"></a>Hinweise

Diese Funktion stellt Excel standardmäßig **WndProc** wiederherstellen die Adresse, die von **HookExcelWindow()** gespeichert wurde mithilfe von **SetWindowLong()** wieder her.
  
### <a name="example"></a>Beispiel

Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

