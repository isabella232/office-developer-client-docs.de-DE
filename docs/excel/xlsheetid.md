---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- Xlsheetid-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e4e184d4e456ffe26292fe31b1b41463834216f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790612"
---
# <a name="xlsheetid"></a>xlSheetId

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Sucht nach der Blatt-ID eines benannten Blatts, um externe Verweise zu erstellen.
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a>Parameter

_pxSheetName_ (**XltypeStr**)
  
(Optional). Der Name des Adressbuchs und Blatt, das Sie informieren möchten. Wenn Length angegeben, gibt die Funktion **XlSheetId** Blatt-ID des Blatts aktiv (vorne) zurück. 
  
## <a name="return-value"></a>R�ckgabewert

Gibt die Blatt-ID im _PxRes -\>val.mref.idSheet_. 
  
> [!NOTE]
> Die _PxRes -\>val.mref.lpmref_ Array Zeiger ist auf NULL festgelegt wurde nach diesem Aufruf, damit besteht keine Notwendigkeit Aufrufen **XlFree** , um den Arbeitsspeicher, die normalerweise dieses Typs enthält, freizugeben, obwohl es dazu vollständig sicher ist. 
  
## <a name="remarks"></a>Hinweise

Die Arbeitsmappe mit dem angegebenen Blatt muss diese Funktion geöffnet sein. Es ist nicht möglich, einen Verweis auf eine nicht geöffneten Arbeitsmappe aus einer DLL zu erstellen. Weitere Informationen zur Verwendung von **XlSheetId** zum Referenzen zu erzeugen finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md) Beispiele für **XltypeRef** zuzugreifen. 
  
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
- [C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

