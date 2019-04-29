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
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a2ca1bb478c5c985ad7032e30ed0cfe3aef31406
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428431"
---
# <a name="xlsheetid"></a>xlSheetId

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Sucht die Blatt-ID eines benannten Blatts, um externe Verweise zu erstellen.
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a>Parameter

_pxSheetName_ (**xltypeStr**)
  
(Optional). Der Name des Buches und des Blatts, über das Sie sich informieren möchten. Wenn kein Wert angegeben wird, gibt die **XLSHEETID** -Funktion die Blatt-ID des aktiven (Front-) Blatts zurück. 
  
## <a name="return-value"></a>Rückgabewert

Gibt die Blatt-ID in _pxRes\>-Val. mref. idSheet_zurück. 
  
> [!NOTE]
> Der _pxRes-\>Val. mref. lpmref-_ Array Zeiger wird nach diesem Aufruf auf NULL festgelegt, sodass es nicht erforderlich ist, **xlFree** aufzurufen, um den von diesem Typ normalerweise enthaltenen Speicher freizugeben, obwohl dies vollständig sicher ist. 
  
## <a name="remarks"></a>Bemerkungen

Die Arbeitsmappe mit dem angegebenen Blatt muss geöffnet sein, um diese Funktion verwenden zu können. Es gibt keine Möglichkeit, einen Verweis auf eine nicht geöffnete Arbeitsmappe aus einer DLL zu erstellen. Weitere Informationen zur Verwendung von **xlSheetId** zum Erstellen von Verweisen finden Sie unter [Memory Management in Excel](memory-management-in-excel.md) for examples of **externen xltypeRef** Construction. 
  
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

