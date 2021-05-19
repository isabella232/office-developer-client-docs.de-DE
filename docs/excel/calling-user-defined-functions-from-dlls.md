---
title: Aufrufen von benutzerdefinierten Funktionen aus DLLs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- udfs [excel 2007], aufrufen von dlls,benutzerdefinierte Funktionen [Excel 2007], Aufrufen von DLLs,DLLs [Excel 2007], Aufrufen von UDFs
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
# <a name="calling-user-defined-functions-from-dlls"></a><span data-ttu-id="5d600-104">Aufrufen von benutzerdefinierten Funktionen aus DLLs</span><span class="sxs-lookup"><span data-stu-id="5d600-104">Calling user-defined functions from DLLs</span></span>

<span data-ttu-id="5d600-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5d600-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5d600-106">Das Aufrufen von benutzerdefinierten Funktionen (USERFs) aus einem Arbeitsblatt ist so einfach wie das Aufrufen integrierter Funktionen: Sie geben die Funktion über eine Zellformel ein.</span><span class="sxs-lookup"><span data-stu-id="5d600-106">Calling user-defined functions (UDFs) from a worksheet is as simple as calling built-in functions: You enter the function via a cell formula.</span></span> <span data-ttu-id="5d600-107">Aus der C-API sind jedoch keine vordefinierten Funktionscodes für die Rückrufe zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5d600-107">However, from the C API, there are no pre-defined function codes to use with the call-backs.</span></span> <span data-ttu-id="5d600-108">Damit Sie UDFs aufrufen können, exportiert die C-API eine XLL-only-Funktion, die [xlUDF-Funktion.](xludf.md)</span><span class="sxs-lookup"><span data-stu-id="5d600-108">To enable you to call UDFs, the C API exports an XLL-only function, the [xlUDF ](xludf.md) function.</span></span> <span data-ttu-id="5d600-109">Das erste Argument der Funktion ist der Funktionsname als Zeichenfolge, und nachfolgende Argumente sind diejenigen, die die UDF normalerweise erwarten würde.</span><span class="sxs-lookup"><span data-stu-id="5d600-109">The function's first argument is the function name as a string, and subsequent arguments are those that the UDF would normally expect.</span></span> 
  
<span data-ttu-id="5d600-110">Mithilfe der **xlfGetWorkspace-Funktion** mit dem Argument 44 können Sie eine Liste der aktuell registrierten XLL-Add-In-Funktionen und -Befehle abrufen.</span><span class="sxs-lookup"><span data-stu-id="5d600-110">You can obtain a list of the currently registered XLL add-in functions and commands by using the **xlfGetWorkspace** function with the argument 44.</span></span> <span data-ttu-id="5d600-111">Dadurch wird ein Array mit drei Spalten zurückgegeben, in dem die Spalten Folgendes darstellen:</span><span class="sxs-lookup"><span data-stu-id="5d600-111">This returns a three-column array where the columns represent the following:</span></span> 
  
- <span data-ttu-id="5d600-112">Der vollständige Pfad und Name der XLL</span><span class="sxs-lookup"><span data-stu-id="5d600-112">The full path and name of the XLL</span></span>
    
- <span data-ttu-id="5d600-113">Der Name der UDF oder des Befehls, wie aus der XLL exportiert</span><span class="sxs-lookup"><span data-stu-id="5d600-113">The name of the UDF or command as exported from the XLL</span></span>
    
- <span data-ttu-id="5d600-114">Die Zeichenfolge für Rückgabe- und Argumentcode</span><span class="sxs-lookup"><span data-stu-id="5d600-114">The return and argument code string</span></span>
    
> [!NOTE]
> <span data-ttu-id="5d600-115">Der aus der XLL exportierte Name ist möglicherweise nicht mit dem registrierten Namen identisch, mit dem Excel UDF oder Befehl kennt.</span><span class="sxs-lookup"><span data-stu-id="5d600-115">The name as exported from the XLL might not be the same as the registered name by which Excel knows the UDF or command.</span></span> 
  
<span data-ttu-id="5d600-116">Ab Excel 2007 sind die #A0 (Analysis Toolpak) vollständig integriert, und die C-API verfügt über eigene Enumerationen für Funktionen wie PRICE, **xlfPrice**.</span><span class="sxs-lookup"><span data-stu-id="5d600-116">Starting in Excel 2007, the Analysis Toolpak (ATP) functions are fully integrated, and the C API has its own enumerations for functions such as PRICE, **xlfPrice**.</span></span> <span data-ttu-id="5d600-117">In früheren Versionen mussten Sie **xlUDF** zum Aufrufen dieser Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="5d600-117">In earlier versions, you had to use **xlUDF** to call these functions.</span></span> <span data-ttu-id="5d600-118">Wenn Ihr Add-In mit den Versionen Excel 2003 und Excel 2007 oder höher arbeiten muss und diese Funktionen verwendet werden, sollten Sie die aktuelle Version erkennen und die Funktion auf die entsprechende Weise aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5d600-118">If your add-in needs to work with Excel 2003 and Excel 2007 or later versions, and it uses these functions, you should detect the current version and call the function in the appropriate way.</span></span> 
  
## <a name="examples"></a><span data-ttu-id="5d600-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d600-119">Examples</span></span>

<span data-ttu-id="5d600-120">Das folgende Beispiel zeigt die **xlUDF-Funktion,** die zum Aufrufen der ATP-Funktion **PRICE** verwendet wird, wenn die ausführungsversion von Excel 2003 oder früher ist.</span><span class="sxs-lookup"><span data-stu-id="5d600-120">The following example shows the **xlUDF** function being used to call the ATP function **PRICE** when the running version of Excel is 2003 or earlier.</span></span> <span data-ttu-id="5d600-121">Informationen zur Einstellung einer globalen Versionsvariablen, z. B. **gExcelVersion12plus** in diesem Beispiel, finden Sie unter [Backward Compatibility](backward-compatibility.md).</span><span class="sxs-lookup"><span data-stu-id="5d600-121">For information about the setting of a global version variable, such as **gExcelVersion12plus** in this example, see [Backward Compatibility](backward-compatibility.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="5d600-122">In diesem Beispiel werden die **Framework-Funktionen TempNum**, **TempStrConst** zum Einrichten der Argumente und Excel zum Aufrufen der C-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d600-122">This example uses the Framework functions **TempNum**, **TempStrConst** to set up the arguments and Excel to call the C API.</span></span> 
  
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

<span data-ttu-id="5d600-123">Wenn Sie eine XLL-Funktion aufrufen, die einen Wert zurückgibt, indem Sie ein Argument ändern, gibt die **xlUDF-Funktion** weiterhin den Wert über die Adresse des Ergebnisses **XLOPER/XLOPER12 zurück.**</span><span class="sxs-lookup"><span data-stu-id="5d600-123">Where you are calling an XLL function that returns a value by modifying an argument in place, the **xlUDF** function still returns the value via the address of the result **XLOPER/XLOPER12**.</span></span> <span data-ttu-id="5d600-124">Mit anderen Worten, das Ergebnis wird wie über eine normale Rückgabe-Anweisung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5d600-124">In other words, the result is returned as if through a normal return statement.</span></span> <span data-ttu-id="5d600-125">**XlOPER/XLOPER12,** das dem Argument entspricht, das für den Rückgabewert verwendet wird, ist unverändert.</span><span class="sxs-lookup"><span data-stu-id="5d600-125">The **XLOPER/XLOPER12** that corresponds to the argument that is used for the return value is unmodified.</span></span> <span data-ttu-id="5d600-126">Betrachten Sie beispielsweise die folgenden beiden UDFs.</span><span class="sxs-lookup"><span data-stu-id="5d600-126">For example, consider the following two UDFs.</span></span> 
  
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

<span data-ttu-id="5d600-127">Wenn **UDF \_ 2** **UDF \_ 1** aufruft, bleibt der Wert von **pxArg** nach dem Aufruf von **Excel12** unverändert, und der von **UDF_1** zurückgegebene Wert ist in **xRetVal enthalten.**</span><span class="sxs-lookup"><span data-stu-id="5d600-127">When **UDF\_2** calls **UDF\_1**, the value of **pxArg** is unchanged after the call to **Excel12**, and the value returned by **UDF_1** is contained in **xRetVal**.</span></span>
  
<span data-ttu-id="5d600-128">Wenn Sie eine große Anzahl von Aufrufen an eine UDF auf diese Weise machen, können Sie den Funktionsnamen zuerst mithilfe der [xlfEvaluate-Funktion auswerten.](xlfevaluate.md)</span><span class="sxs-lookup"><span data-stu-id="5d600-128">When you are making a large number of calls to a UDF in this way, you can evaluate the function name first by using the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="5d600-129">Die resultierende Zahl, die mit der Registrierungs-ID identisch ist, die von der **xlfRegister-Funktion** zurückgegeben wird, kann an Stelle des Funktionsnamens als erstes Argument an die **xlUDF-Funktion übergeben** werden.</span><span class="sxs-lookup"><span data-stu-id="5d600-129">The resulting number, which is the same as the registration ID that is returned by the **xlfRegister** function, can be passed in place of the function name as the first argument to the **xlUDF** function.</span></span> <span data-ttu-id="5d600-130">Dadurch können Excel die Funktion schneller finden und aufrufen, als wenn sie den Funktionsnamen jedes Mal nachschauen muss.</span><span class="sxs-lookup"><span data-stu-id="5d600-130">This enables Excel to find and call the function more quickly than if it has to look up the function name every time.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5d600-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d600-131">See also</span></span>

- [<span data-ttu-id="5d600-132">Zulassen von Benutzerunterbrechungen bei langwierigen Vorgängen</span><span class="sxs-lookup"><span data-stu-id="5d600-132">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
- [<span data-ttu-id="5d600-133">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="5d600-133">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [<span data-ttu-id="5d600-134">Erste Schritte mit dem Excel XLL SDK</span><span class="sxs-lookup"><span data-stu-id="5d600-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

