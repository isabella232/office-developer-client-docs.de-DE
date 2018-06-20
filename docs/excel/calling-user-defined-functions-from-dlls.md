---
title: Aufrufen benutzerdefinierter Funktionen von DLLs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- UDFs [excel 2007], Aufrufen aus Dlls, benutzerdefinierte Funktionen [Excel 2007], Aufrufen aus DLLs DLLs [Excel 2007], Aufrufen von UDFs
localization_priority: Normal
ms.assetid: 99a37108-0083-4240-9c6a-3afa8d7a04f6
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4e893cf1e54489610315dd5c5d57bd78c3c936d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790399"
---
# <a name="calling-user-defined-functions-from-dlls"></a>Aufrufen benutzerdefinierter Funktionen von DLLs

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Aufrufen von benutzerdefinierten Funktionen (UDFs) in einem Arbeitsblatt ist so einfach wie integrierte Funktionen aufrufen: Geben Sie die Funktion über eine Zellformel. Aus der C-API sind jedoch keine vordefinierte Funktionscodes mit der Rückrufe verwenden. Damit Sie UDFs aufrufen können, exportiert der C-API eine XLL-only-Funktion, die [XlUDF](xludf.md) -Funktion. Die Funktion erste Argument ist der Funktionsname als Zeichenfolge und nachfolgende Argumente sind die, die die UDF normalerweise erwarten. 
  
Sie können eine Liste der derzeit registrierten XLL-add-in-Funktionen und Befehle abrufen, indem Sie mit der **XlfGetWorkspace** -Funktion und das Argument 44. Diese drei Spalten gibt ein Array zurück, wobei die Spalten Folgendes darstellen: 
  
- Den vollständigen Pfad und Namen der XLL
    
- Der Name der UDF oder Befehl wie aus der XLL exportiert
    
- Die Zeichenfolge Return und argument
    
> [!NOTE]
> Der Name als aus der XLL exportiert identisch mit dem registrierten Namen möglicherweise nicht mit dem Excel die UDF oder den Befehl bekannt ist. 
  
Ab Excel 2007, die Funktionen (Analysis Toolpak, ATP) sind vollständig integriert und der C-API hat eine eigene Enumerationen um Funktionen wie beispielsweise Preis **XlfPrice**. In früheren Versionen mussten Sie **XlUDF** verwenden, um diese Funktionen aufrufen. Wenn Ihr Add-in Excel 2003 und Excel 2007 oder höher entwickelt muss, und diese Funktionen verwendet, sollten Sie die aktuelle Version erkennen und rufen die Funktion entsprechend. 
  
## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die **XlUDF** -Funktion verwendet wird, um die ATP-Funktion **Preis** aufrufen, wenn die ausgeführte Version von Excel 2003 oder früher ist. Informationen zur Einstellung einer globalen Version Variablen, wie beispielsweise **gExcelVersion12plus** in diesem Beispiel finden Sie unter [Abwärtskompatibilität](backward-compatibility.md).
  
> [!NOTE]
> In diesem Beispiel wird die Framework-Funktionen **TempNum**, **TempStrConst** , um die Argumente und Excel einzurichten, der C-API-aufrufen. 
  
```C
LPXLOPER TempNum(double d);
LPXLOPER TempStrConst(const LPSTR lpstr);
int cdecl Excel(int xlfn, LPXLOPER pxResult, int count, ...);
double call_ATP_example(void)
{
  XLOPER xPrice;
  int xl_ret_val;
  if(gExcelVersion12plus) // Starting in Excel 2007
  {
    xl_ret_val = Excel(xlfPrice, &xPrice, 7,
      TempNum(39084.0), // settlement date 2-Jan-2007
      TempNum(46706.0), // maturity date 15-Nov-2027
      TempNum(0.04), // Coupon
      TempNum(0.05), // Yield
      TempNum(1.0), // redemption value: 100% of face
      TempNum(1.0), // Annual coupons
      TempNum(1.0)); // Rate basis Act/Act
  }
  else // Excel 2003-
  {
    xl_ret_val = Excel(xlUDF, &xPrice, 8,
      TempStrConst("PRICE"),
      TempNum(39084.0), // settlement date 2-Jan-2007
      TempNum(46706.0), // maturity date 15-Nov-2027
      TempNum(0.04), // Coupon
      TempNum(0.05), // Yield
      TempNum(1.0), // redepmtion value: 100% of face
      TempNum(1.0), // Annual coupons
      TempNum(1.0)); // Rate basis Act/Act
  }
  if(xl_ret_val != xlretSuccess || xPrice.xltype != xltypeNum)
  {
// Even though PRICE is not expected to return a string, there
// is no harm in freeing the XLOPER to be safe
    Excel(xlFree, 0, 1, &xPrice);
    return -1.0; // an error value
  }
  return xPrice.val.num;
}
```

<br/>

In dem Sie eine XLL-Funktion aufrufen, die ein Wert zurückgegeben, indem ein Argument an, die Funktion **XlUDF** ändern gibt den Wert weiterhin über die Adresse des Ergebnisses **XLOPER/XLOPER12**zurück. Anders ausgedrückt, wird das Ergebnis als würde über eine normale return-Anweisung zurückgegeben. **XLOPER/XLOPER12** , die das Argument entspricht, die für den Rückgabewert verwendet wird, ist unverändert. Betrachten Sie beispielsweise den folgenden zwei UDFs. 
  
```C
// Registered as "1E". Returns its argument incremented by 1.
void WINAPI UDF_1(double *pArg)
{
  *pArg += 1.0;
}
// Registered as "QQ". Returns its argument unmodified
// unless it is a number, in which case it increments it
// by calling UDF_1.
LPXLOPER12 WINAPI UDF_2(LPXLOPER12 pxArg)
{
  static XLOPER12 xRetVal; // Not thread-safe
  XLOPER12 xFn;
  xFn.xltype = xltypeStr;
  xFn.val.str = L"\005UDF_1";
  Excel12(xlUDF, &xRetVal, 2, &xFn, pxArg);
  xRetVal.xltype |= xlbitXLFree;
  return &xRetVal;
}
```

Wenn **UDF\_2** Anrufe **UDF\_1**, wird des Werts der **PxArg** nach dem Aufruf von **Excel12**unverändert und der von **UDF_1** zurückgegebene Wert in **xRetVal**enthalten ist.
  
Wenn Sie eine große Anzahl von Anrufen für eine UDF auf diese Weise herstellen, können Sie den Namen der Funktion mithilfe der [XlfEvaluate-Funktion](xlfevaluate.md)zuerst auswerten. Die resultierende Zahl, die die Registrierung ID identisch, die von der Funktion **XlfRegister** zurückgegeben wird ist, kann an die Funktion **XlUDF** anstelle der Funktionsname als erstes Argument übergeben werden. Auf diese Weise können Excel zu suchen, und rufen die Funktion schneller als hat, wenn sie den Namen der Funktion jedes Mal nachzuschlagen. 
  
## <a name="see-also"></a>Siehe auch

- [Genehmigungsverfahren Benutzer Zeilenumbr�che in langen Vorg�nge](permitting-user-breaks-in-lengthy-operations.md)
- [C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [Erste Schritte mit Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

