---
title: Aufrufen von benutzerdefinierten Funktionen aus DLLs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- UDFs [Excel 2007], Aufrufen von DLLs, benutzerdefinierten Funktionen [Excel 2007], Aufrufen von DLLs, DLLs [Excel 2007], Aufrufen von UDFs
localization_priority: Normal
ms.assetid: 99a37108-0083-4240-9c6a-3afa8d7a04f6
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9e2ca3f4485fb41c5ab6a48f323b4c0093e747e4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417945"
---
# <a name="calling-user-defined-functions-from-dlls"></a>Aufrufen von benutzerdefinierten Funktionen aus DLLs

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Das Aufrufen von benutzerdefinierten Funktionen (User-Defined Functions, UDFs) aus einem Arbeitsblatt ist so einfach wie das Aufrufen integrierter Funktionen: Sie geben die Funktion über eine Zellformel ein. Aus der C-API können jedoch keine vordefinierten Funktionscodes für die Rückrufe verwendet werden. Damit Sie UDFs aufrufen können, exportiert die C-API eine nur-XLL-Funktion, die [xlUDF](xludf.md) -Funktion. Das erste Argument der Funktion ist der Funktionsname als Zeichenfolge, und nachfolgende Argumente sind die, die die UDF normalerweise erwarten würde. 
  
Sie können eine Liste der derzeit registrierten XLL-Add-in-Funktionen und-Befehle abrufen, indem Sie die **xlfGetWorkspace** -Funktion mit dem Argument 44 verwenden. Dadurch wird ein Array mit drei Spalten zurückgegeben, in dem die Spalten Folgendes darstellen: 
  
- Der vollständige Pfad und Name der XLL
    
- Der Name des UDF oder Befehls, der aus der XLL exportiert wurde.
    
- Die Rückgabe-und Argument Codezeichenfolge
    
> [!NOTE]
> Der Name, der aus der XLL exportiert wurde, ist möglicherweise nicht identisch mit dem registrierten Namen, mit dem Excel das UDF oder den Befehl kennt. 
  
Ab Excel 2007 sind die Funktionen von Analysis-Funktionen (ATP) vollständig integriert, und die C-API verfügt über eigene Enumerationen für Funktionen wie PRICE, **xlfPrice**. In früheren Versionen mussten Sie **xlUDF** verwenden, um diese Funktionen aufzurufen. Wenn Ihr Add-in mit Excel 2003 und Excel 2007 oder höher arbeiten muss und diese Funktionen verwendet, sollten Sie die aktuelle Version feststellen und die Funktion auf die entsprechende Weise aufrufen. 
  
## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die **xlUDF** -Funktion, die verwendet wird, um den ATP-Funktions **Preis** aufzurufen, wenn die laufende Version von Excel 2003 oder früher ist. Informationen zur Einstellung einer globalen Versions Variablen wie **gExcelVersion12plus** in diesem Beispiel finden Sie unter [Abwärtskompatibilität](backward-compatibility.md).
  
> [!NOTE]
> In diesem Beispiel werden die Frameworkfunktionen **TempNum**, **TempStrConst** zum Einrichten der Argumente und Excel zum Aufrufen der C-API verwendet. 
  
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

Wenn Sie eine XLL-Funktion aufrufen, die einen Wert zurückgibt, indem Sie ein Argument ändern, gibt die **xlUDF** -Funktion den Wert weiterhin über die Adresse des Ergebnisses **XLOPER/XLOPER12**zurück. Anders ausgedrückt, wird das Ergebnis wie durch eine normale Return-Anweisung zurückgegeben. Die **XLOPER/XLOPER12** , die dem Argument entspricht, das für den Rückgabewert verwendet wird, ist unverändert. Betrachten Sie beispielsweise die folgenden beiden UDFs. 
  
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

Wenn **UDF\_2** **UDF\_1**aufruft, ist der Wert von **pxArg** nach dem Aufruf von **Excel12**unverändert, und der von **UDF_1** zurückgegebene Wert ist in **xRetVal**enthalten.
  
Wenn Sie eine hohe Anzahl von Aufrufen an eine UDF auf diese Weise durchführen, können Sie den Funktionsnamen zuerst mithilfe der XlfEvaluate- [Funktion](xlfevaluate.md)auswerten. Die resultierende Zahl, die mit der Registrierungs-ID identisch ist, die von der **xlfRegister** -Funktion zurückgegeben wird, kann anstelle des Funktionsnamens als erstes Argument an die **xlUDF** -Funktion übergeben werden. Dies ermöglicht Excel, die Funktion schneller zu finden und aufzurufen, als wenn Sie immer den Funktionsnamen nachschlagen muss. 
  
## <a name="see-also"></a>Siehe auch

- [Zulassen von Benutzerunterbrechungen bei langwierigen Vorgängen](permitting-user-breaks-in-lengthy-operations.md)
- [C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [Erste Schritte mit dem Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

