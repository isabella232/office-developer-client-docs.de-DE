---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- hookexcelwindow-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4103bf3a95388d20efeb74fcd736aeb5520d0845
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413507"
---
# <a name="hookexcelwindow"></a>HookExcelWindow

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Installiert **ExcelCursorProc** so, dass es vor dem Microsoft Excel **WndProc aufgerufen wird.**
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parameter

 _hWndExcel_ (**HANDLE**)
  
Das Excel-Windows-Handle.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion gibt keinen Wert zurück.
  
## <a name="remarks"></a>Hinweise

Die Funktion ruft die Adresse des Excel **WndProc** über die Verwendung von **GetWindowLong() ab.** Er speichert diesen Wert in einer globalen Datei, die zum Aufrufen des **Standard-WndProc** und zum Wiederherstellen verwendet werden kann. Schließlich wird diese Adresse durch die Adresse von **ExcelCursorProc** mithilfe von **SetWindowLong() ersetzt.**
  
### <a name="example"></a>Beispiel

Den  `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

