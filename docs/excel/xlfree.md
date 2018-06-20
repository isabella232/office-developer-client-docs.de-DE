---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- XlFree-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2dd61ee5cd0e2e671cc47425689287b8a437732f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790607"
---
# <a name="xlfree"></a>xlFree

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Verwendet, um Ressourcen, die von Microsoft Excel beim Erstellen der Rückgabe Wert **XLOPER**Arbeitsspeicher freizugeben/ **XLOPER12** in einem Aufruf von [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)oder [Excel12v](excel4v-excel12v.md). **XlFree** -Funktion gibt den zusätzlichen Arbeitsspeicher frei und setzt den Zeiger auf **einen Nullwert fest** , jedoch ist nicht Teil der **XLOPER**zerstören/ **XLOPER12**.
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a>Parameter

 _px_1,..., px_n_
  
Eine oder mehrere **XLOPER**/ **XLOPER12**s freigegeben werden. In Excel-Versionen bis zu 2003 ist die maximale Anzahl von Zeigern übergeben werden kann, die 30. Ab Excel 2007, wird dies auf 255 erhöht.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Diese Funktion gibt keinen Wert zurück.
  
## <a name="remarks"></a>Hinweise

Sie müssen alle **XLOPER** , die Sie als Rückgabewert von **Excel4** oder **Excel4v** erhalten und jeder **XLOPER12** , die Sie als Rückgabewert aus der **Excel12** oder **Excel12v** abrufen, wenn sie einen der folgenden Typen sind frei: **XltypeStr **, **XltypeMulti**oder **XltypeRef**. Es ist sicherer, andere Typen freizugeben, auch wenn sie keine zusätzlichen Arbeitsspeicher verwenden, solange Sie diese von **Excel4** oder **Excel12**erhalten haben.
  
In dem Sie zurückgeben nach Excel eines Zeigers auf eine **XLOPER**/ **XLOPER12** , das Excel-reservierter Speicher freigegeben werden weiterhin enthält, muss die **XlbitXLFree** Excel-Versionen des Speichers sicherstellen festgelegt. 
  
## <a name="example"></a>Beispiel

Dieses Beispiel ruft **erhalten möchten. WORKSPACE(1)** die Plattform zurückgegeben, auf welche Excel als Zeichenfolge ausgeführt wird. Diesem zurückgegebenen Zeichenfolge in einen Puffer zur späteren Verwendung kopiert. Der Code einfügt den Puffer wieder in **XLOPER12** zur späteren Verwendung mit der Excel-Funktion. Abschließend zeigt der Code die Zeichenfolge in einer Warnung an. 
  
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

- [C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

