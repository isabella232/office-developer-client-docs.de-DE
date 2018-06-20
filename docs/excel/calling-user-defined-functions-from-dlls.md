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
# <a name="calling-user-defined-functions-from-dlls"></a><span data-ttu-id="3bdfe-104">Aufrufen benutzerdefinierter Funktionen von DLLs</span><span class="sxs-lookup"><span data-stu-id="3bdfe-104">Calling user-defined functions from DLLs</span></span>

<span data-ttu-id="3bdfe-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3bdfe-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3bdfe-106">Aufrufen von benutzerdefinierten Funktionen (UDFs) in einem Arbeitsblatt ist so einfach wie integrierte Funktionen aufrufen: Geben Sie die Funktion über eine Zellformel.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-106">Calling user-defined functions (UDFs) from a worksheet is as simple as calling built-in functions: You enter the function via a cell formula.</span></span> <span data-ttu-id="3bdfe-107">Aus der C-API sind jedoch keine vordefinierte Funktionscodes mit der Rückrufe verwenden.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-107">However, from the C API, there are no pre-defined function codes to use with the call-backs.</span></span> <span data-ttu-id="3bdfe-108">Damit Sie UDFs aufrufen können, exportiert der C-API eine XLL-only-Funktion, die [XlUDF](xludf.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-108">To enable you to call UDFs, the C API exports an XLL-only function, the [xlUDF ](xludf.md) function.</span></span> <span data-ttu-id="3bdfe-109">Die Funktion erste Argument ist der Funktionsname als Zeichenfolge und nachfolgende Argumente sind die, die die UDF normalerweise erwarten.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-109">The function's first argument is the function name as a string, and subsequent arguments are those that the UDF would normally expect.</span></span> 
  
<span data-ttu-id="3bdfe-110">Sie können eine Liste der derzeit registrierten XLL-add-in-Funktionen und Befehle abrufen, indem Sie mit der **XlfGetWorkspace** -Funktion und das Argument 44.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-110">You can obtain a list of the currently registered XLL add-in functions and commands by using the **xlfGetWorkspace** function with the argument 44.</span></span> <span data-ttu-id="3bdfe-111">Diese drei Spalten gibt ein Array zurück, wobei die Spalten Folgendes darstellen:</span><span class="sxs-lookup"><span data-stu-id="3bdfe-111">This returns a three-column array where the columns represent the following:</span></span> 
  
- <span data-ttu-id="3bdfe-112">Den vollständigen Pfad und Namen der XLL</span><span class="sxs-lookup"><span data-stu-id="3bdfe-112">The full path and name of the XLL</span></span>
    
- <span data-ttu-id="3bdfe-113">Der Name der UDF oder Befehl wie aus der XLL exportiert</span><span class="sxs-lookup"><span data-stu-id="3bdfe-113">The name of the UDF or command as exported from the XLL</span></span>
    
- <span data-ttu-id="3bdfe-114">Die Zeichenfolge Return und argument</span><span class="sxs-lookup"><span data-stu-id="3bdfe-114">The return and argument code string</span></span>
    
> [!NOTE]
> <span data-ttu-id="3bdfe-115">Der Name als aus der XLL exportiert identisch mit dem registrierten Namen möglicherweise nicht mit dem Excel die UDF oder den Befehl bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-115">The name as exported from the XLL might not be the same as the registered name by which Excel knows the UDF or command.</span></span> 
  
<span data-ttu-id="3bdfe-116">Ab Excel 2007, die Funktionen (Analysis Toolpak, ATP) sind vollständig integriert und der C-API hat eine eigene Enumerationen um Funktionen wie beispielsweise Preis **XlfPrice**.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-116">Starting in Excel 2007, the Analysis Toolpak (ATP) functions are fully integrated, and the C API has its own enumerations for functions such as PRICE, **xlfPrice**.</span></span> <span data-ttu-id="3bdfe-117">In früheren Versionen mussten Sie **XlUDF** verwenden, um diese Funktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-117">In earlier versions, you had to use **xlUDF** to call these functions.</span></span> <span data-ttu-id="3bdfe-118">Wenn Ihr Add-in Excel 2003 und Excel 2007 oder höher entwickelt muss, und diese Funktionen verwendet, sollten Sie die aktuelle Version erkennen und rufen die Funktion entsprechend.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-118">If your add-in needs to work with Excel 2003 and Excel 2007 or later versions, and it uses these functions, you should detect the current version and call the function in the appropriate way.</span></span> 
  
## <a name="examples"></a><span data-ttu-id="3bdfe-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3bdfe-119">Examples</span></span>

<span data-ttu-id="3bdfe-120">Das folgende Beispiel zeigt die **XlUDF** -Funktion verwendet wird, um die ATP-Funktion **Preis** aufrufen, wenn die ausgeführte Version von Excel 2003 oder früher ist.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-120">The following example shows the **xlUDF** function being used to call the ATP function **PRICE** when the running version of Excel is 2003 or earlier.</span></span> <span data-ttu-id="3bdfe-121">Informationen zur Einstellung einer globalen Version Variablen, wie beispielsweise **gExcelVersion12plus** in diesem Beispiel finden Sie unter [Abwärtskompatibilität](backward-compatibility.md).</span><span class="sxs-lookup"><span data-stu-id="3bdfe-121">For information about the setting of a global version variable, such as **gExcelVersion12plus** in this example, see [Backward Compatibility](backward-compatibility.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="3bdfe-122">In diesem Beispiel wird die Framework-Funktionen **TempNum**, **TempStrConst** , um die Argumente und Excel einzurichten, der C-API-aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-122">This example uses the Framework functions **TempNum**, **TempStrConst** to set up the arguments and Excel to call the C API.</span></span> 
  
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

<span data-ttu-id="3bdfe-123">In dem Sie eine XLL-Funktion aufrufen, die ein Wert zurückgegeben, indem ein Argument an, die Funktion **XlUDF** ändern gibt den Wert weiterhin über die Adresse des Ergebnisses **XLOPER/XLOPER12**zurück.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-123">Where you are calling an XLL function that returns a value by modifying an argument in place, the **xlUDF** function still returns the value via the address of the result **XLOPER/XLOPER12**.</span></span> <span data-ttu-id="3bdfe-124">Anders ausgedrückt, wird das Ergebnis als würde über eine normale return-Anweisung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-124">In other words, the result is returned as if through a normal return statement.</span></span> <span data-ttu-id="3bdfe-125">**XLOPER/XLOPER12** , die das Argument entspricht, die für den Rückgabewert verwendet wird, ist unverändert.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-125">The **XLOPER/XLOPER12** that corresponds to the argument that is used for the return value is unmodified.</span></span> <span data-ttu-id="3bdfe-126">Betrachten Sie beispielsweise den folgenden zwei UDFs.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-126">For example, consider the following two UDFs.</span></span> 
  
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

<span data-ttu-id="3bdfe-127">Wenn **UDF\_2** Anrufe **UDF\_1**, wird des Werts der **PxArg** nach dem Aufruf von **Excel12**unverändert und der von **UDF_1** zurückgegebene Wert in **xRetVal**enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-127">When **UDF\_2** calls **UDF\_1**, the value of **pxArg** is unchanged after the call to **Excel12**, and the value returned by **UDF_1** is contained in **xRetVal**.</span></span>
  
<span data-ttu-id="3bdfe-128">Wenn Sie eine große Anzahl von Anrufen für eine UDF auf diese Weise herstellen, können Sie den Namen der Funktion mithilfe der [XlfEvaluate-Funktion](xlfevaluate.md)zuerst auswerten.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-128">When you are making a large number of calls to a UDF in this way, you can evaluate the function name first by using the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="3bdfe-129">Die resultierende Zahl, die die Registrierung ID identisch, die von der Funktion **XlfRegister** zurückgegeben wird ist, kann an die Funktion **XlUDF** anstelle der Funktionsname als erstes Argument übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-129">The resulting number, which is the same as the registration ID that is returned by the **xlfRegister** function, can be passed in place of the function name as the first argument to the **xlUDF** function.</span></span> <span data-ttu-id="3bdfe-130">Auf diese Weise können Excel zu suchen, und rufen die Funktion schneller als hat, wenn sie den Namen der Funktion jedes Mal nachzuschlagen.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-130">This enables Excel to find and call the function more quickly than if it has to look up the function name every time.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3bdfe-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bdfe-131">See also</span></span>

- [<span data-ttu-id="3bdfe-132">Genehmigungsverfahren Benutzer Zeilenumbr�che in langen Vorg�nge</span><span class="sxs-lookup"><span data-stu-id="3bdfe-132">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
- [<span data-ttu-id="3bdfe-133">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen</span><span class="sxs-lookup"><span data-stu-id="3bdfe-133">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [<span data-ttu-id="3bdfe-134">Erste Schritte mit Excel XLL SDK</span><span class="sxs-lookup"><span data-stu-id="3bdfe-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

