---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- xlFree-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: de1c75ad65acacd44644e9bfb111b30abd0a578e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424714"
---
# <a name="xlfree"></a>xlFree

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird verwendet, um von Microsoft Excel zugewiesene Speicherressourcen freizugeben, wenn der Rückgabewert **XLOPER**/ **XLOPER12** bei einem Aufruf von [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)oder [Excel12v](excel4v-excel12v.md)erstellt wird. Die **xlFree** -Funktion gibt den hilfsspeicher frei und setzt den Zeiger auf **null** , aber andere Teile des **XLOPER**/ -**XLOPER12**werden nicht gelöscht.
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a>Parameter

 _px_1,..., px_n_
  
Mindestens ein **XLOPER**/ -**XLOPER12**, das freigegeben werden soll. In Excel-Versionen bis zu 2003 ist die maximale Anzahl von Zeigern, die übergeben werden können, 30. Ab Excel 2007 wird dieser Wert auf 255 erhöht.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Diese Funktion gibt keinen Wert zurück.
  
## <a name="remarks"></a>Bemerkungen

Sie müssen jedes **XLOPER** freigeben, das Sie als Rückgabewert aus **Excel4** oder **Excel4v** und jeder **XLOPER12** erhalten, die Sie als Rückgabewert von **Excel12** oder **Excel12v** erhalten, wenn Sie einen der folgenden Typen aufweisen: **xltypeStr **, **XltypeMulti**oder **externen xltypeRef**. Es ist immer sicher, andere Typen freizugeben, auch wenn Sie keinen zusätzlichen Speicher verwenden, solange Sie von **Excel4** oder **Excel12**.
  
Wenn Sie zu Excel einen Zeiger auf eine **XLOPER**/ -**XLOPER12** zurückgeben, die noch zu enthaltenden Excel-Arbeitsspeicher enthält, müssen Sie die **xlbitXLFree** festlegen, um sicherzustellen, dass Excel den Arbeitsspeicher freigibt. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird **Get aufgerufen. Arbeitsbereich (1)** , um die Plattform zurückzugeben, auf der Excel derzeit als Zeichenfolge läuft. Der Code kopiert diese zurückgegebene Zeichenfolge zur späteren Verwendung in einen Puffer. Der Code platziert den Puffer wieder in der **XLOPER12** für die spätere Verwendung mit der Excel-Funktion. Schließlich zeigt der Code die Zeichenfolge in einem Warnungsfeld an. 
  
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

