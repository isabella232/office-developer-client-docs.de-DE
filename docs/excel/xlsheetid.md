---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- xlsheetid-Funktion [Excel 2007]
ms.localizationpriority: medium
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 34dc592d0f6dae54c73d37bd85d125168d0d9dc1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552157"
---
# <a name="xlsheetid"></a>xlSheetId

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Sucht die Blatt-ID eines benannten Blatts, um externe Verweise zu erstellen.
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a>Parameter

_pxSheetName_ (**xltypeStr**)
  
(Optional). Der Name des Buchs und Blatts, über das Sie sich informieren möchten. Wenn dieser Wert weggelassen wird, gibt die **XlSheetId-Funktion** die Blatt-ID des aktiven (vorderen) Blatts zurück. 
  
## <a name="return-value"></a>Rückgabewert

Gibt die Blatt-ID in _pxRes- \> val.mref.idSheet zurück._ 
  
> [!NOTE]
> Der  _pxRes-val.mref.lpmref-Arrayzeiger \>_ wird nach diesem Aufruf auf NULL festgelegt, sodass **xlFree** nicht aufgerufen werden muss, um den Speicher freizugeben, der normalerweise in diesem Typ enthalten ist, obwohl dies völlig sicher ist. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Arbeitsmappe, die das angegebene Blatt enthält, muss geöffnet sein, um diese Funktion verwenden zu können. Es gibt keine Möglichkeit, einen Verweis auf eine nicht geöffnete Arbeitsmappe aus einer DLL zu erstellen. Weitere Informationen zur Verwendung von **xlSheetId** zum Erstellen von Verweisen finden Sie unter [Speicherverwaltung in Excel,](memory-management-in-excel.md) um Beispiele für **die XltypeRef-Konstruktion** zu finden. 
  
## <a name="example"></a>Beispiel

 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetIdExample(void)
{       
   XLOPER12 xSheetName, xRes;
   xSheetName.xltype = xltypeStr;
   xSheetName.val.str = L"\022[BOOK1.XLSX]Sheet1";
   Excel12(xlSheetId, &xRes, 1, (LPXLOPER12)&xSheetName);
   Excel12f(xlcAlert, 0, 1, TempNum12(xRes.val.mref.idSheet));
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>Siehe auch

- [xlSheetNm](xlsheetnm.md)
- [C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

