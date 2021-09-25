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
ms.localizationpriority: medium
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4ded29045ae66d4f4a73b68bc74d695ca8059449
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576709"
---
# <a name="hookexcelwindow"></a>HookExcelWindow

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Installiert **ExcelCursorProc** so, dass es vor dem Microsoft Excel **WndProc-Hauptmodul** aufgerufen wird.
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>Parameter

 _hWndExcel_ (**HANDLE**)
  
Der Excel Haupthandle Windows.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion gibt keinen Wert zurück.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Funktion ruft die Adresse des Excel **WndProc** durch die Verwendung von **GetWindowLong()** ab. Dieser Wert wird in einem globalen Speicher gespeichert, der zum Aufrufen der **Standard-WndProc** und zum Wiederherstellen des Werts verwendet werden kann. Schließlich wird diese Adresse durch die Adresse von **ExcelCursorProc** mithilfe von **SetWindowLong()** ersetzt.
  
### <a name="example"></a>Beispiel

Informationen zum Quellcode für diese Funktion finden Sie  `\SAMPLES\GENERIC\GENERIC.C` unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

