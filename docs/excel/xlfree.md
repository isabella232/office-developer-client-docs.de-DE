---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- xlfree-Funktion [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 99e3305d81f383c5b532828736b42aa5a146b9ed
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564666"
---
# <a name="xlfree"></a>xlFree

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird verwendet, um Speicherressourcen freizugeben, die von Microsoft Excel beim Erstellen des **Rückgabewerts XLOPER** /  **XLOPER12** in einem Aufruf von [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)oder [Excel12v](excel4v-excel12v.md)zugeordnet sind. Die **XlFree-Funktion** gibt den Hilfsspeicher frei und setzt den Zeiger auf **NULL** zurück, zerstört jedoch keine anderen Teile der **XLOPER** /  **XLOPER12**.
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a>Parameter

 _px_1, ..., px_n_
  
Ein oder mehrere **XLOPER** /  **XLOPER12** s, die freigegeben werden sollen. In Excel Versionen bis 2003 beträgt die maximale Anzahl von Zeigern, die übergeben werden können, 30. Ab Excel 2007 wird dies auf 255 erhöht.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Diese Funktion gibt keinen Wert zurück.
  
## <a name="remarks"></a>HinwBemerkungeneise

Sie müssen jeden **XLOPER, den** Sie als Rückgabewert aus **Excel4** oder **Excel4v** erhalten, und jeden **XLOPER12** freigeben, den Sie als Rückgabewert aus **Excel12** oder **Excel12v** erhalten, wenn es sich um einen der folgenden Typen handelt: **xltypeStr**, **xltypeMulti** oder **xltypeRef**. Es ist immer sicher, andere Typen freizugeben, auch wenn sie keinen Zusätzlichen Speicher verwenden, solange Sie sie aus **Excel4** oder **Excel12** erhalten haben.
  
Wenn Sie einen Zeiger auf einen **XLOPER XLOPER12** Excel, der /   noch Excel freigegebenen Arbeitsspeicher enthält, müssen Sie **xlbitXLFree** festlegen, um sicherzustellen, dass Excel den Arbeitsspeicher freigibt. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird **GET aufgerufen. WORKSPACE(1)** zum Zurückgeben der Plattform, auf der Excel derzeit als Zeichenfolge ausgeführt wird. Der Code kopiert diese zurückgegebene Zeichenfolge zur späteren Verwendung in einen Puffer. Der Code platziert den Puffer wieder in **XLOPER12,** um ihn später mit der Excel-Funktion zu verwenden. Schließlich zeigt der Code die Zeichenfolge in einem Warnungsfeld an. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlFreeExample(void)
{
   XLOPER12 xRes, xInt;
   XCHAR buffer[cchMaxStz];
   int i,len;
   // Create an XLOPER12 for the argument to Getworkspace.
   xInt.xltype = xltypeInt;
   xInt.val.w = 1;
   // Call GetWorkspace.
   Excel12f(xlfGetWorkspace, &xRes, 1, (LPXLOPER12)&xInt);
   
   // Get the length of the returned string
   len = (int)xRes.val.str[0];
   //Take into account 1st char, which contains the length
   //and the null terminator. Truncate if necessary to fit
   //buffer.
   if (len > cchMaxStz - 2)
      len = cchMaxStz - 2;
   // Copy to buffer.
   for(i = 1; i <= len; i++)
      buffer[i] = xRes.val.str[i];
   // Null terminate, Not necessary but a good idea.
   buffer[len] = '\0';
   buffer[0] = len;
   // Free the string returned from Excel.
   Excel12f(xlFree, 0, 1, &xRes);
   // Create a new string XLOPER12 for the alert.
   xRes.xltype = xltypeStr;
   xRes.val.str = buffer;
   // Show the alert.
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>Siehe auch

- [C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

