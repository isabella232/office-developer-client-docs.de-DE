---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- xlfree-Funktion [excel 2007]
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
# <a name="xlfree"></a><span data-ttu-id="a8221-104">xlFree</span><span class="sxs-lookup"><span data-stu-id="a8221-104">xlFree</span></span>

 <span data-ttu-id="a8221-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a8221-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a8221-106">Wird zum Freispeichern von von Microsoft Excel beim Erstellen des Rückgabewerts **XLOPER** XLOPER12 in einem Aufruf von /   [Excel4,](excel4-excel12.md) [Excel4v,](excel4v-excel12v.md) [Excel12](excel4-excel12.md)oder [Excel12v](excel4v-excel12v.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="a8221-106">Used to free memory resources allocated by Microsoft Excel when creating the return value **XLOPER**/ **XLOPER12** in a call to [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), or [Excel12v](excel4v-excel12v.md).</span></span> <span data-ttu-id="a8221-107">Die **xlFree-Funktion** gibt den Hilfsspeicher frei und setzt den Zeiger auf **NULL zurück,** zerstört aber keine anderen Teile der **XLOPER** /  **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="a8221-107">The **xlFree** function frees the auxiliary memory and resets the pointer to **NULL** but does not destroy other parts of the **XLOPER**/ **XLOPER12**.</span></span>
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a><span data-ttu-id="a8221-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8221-108">Parameters</span></span>

 <span data-ttu-id="a8221-109">_px_1, ..., px_n_</span><span class="sxs-lookup"><span data-stu-id="a8221-109">_px_1, ..., px_n_</span></span>
  
<span data-ttu-id="a8221-110">Ein oder mehrere **XLOPER** /  **XLOPER12** s, die frei werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a8221-110">One or more **XLOPER**/ **XLOPER12** s to be freed.</span></span> <span data-ttu-id="a8221-111">In Excel bis 2003 beträgt die maximale Anzahl von Zeigern, die übergeben werden können, 30.</span><span class="sxs-lookup"><span data-stu-id="a8221-111">In Excel versions up to 2003, the maximum number of pointers that can be passed is 30.</span></span> <span data-ttu-id="a8221-112">Ab Excel 2007 wird diese Zahl auf 255 erhöht.</span><span class="sxs-lookup"><span data-stu-id="a8221-112">Starting in Excel 2007, this is increased to 255.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a8221-113">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8221-113">Property value/Return value</span></span>

<span data-ttu-id="a8221-114">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a8221-114">This function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8221-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a8221-115">Remarks</span></span>

<span data-ttu-id="a8221-116">Sie müssen alle **XLOPER,** die Sie als Rückgabewert aus **Excel4** oder **Excel4v** erhalten, und alle **XLOPER12,** die Sie als Rückgabewert von **Excel12** oder **Excel12v** erhalten, freigeben, wenn es sich um einen der folgenden Typen handelt: **xltypeStr**, **xltypeMulti** oder **xltypeRef**.</span><span class="sxs-lookup"><span data-stu-id="a8221-116">You must free every **XLOPER** that you get as a return value from **Excel4** or **Excel4v** and every **XLOPER12** that you get as a return value from **Excel12** or **Excel12v** if they are one of the following types: **xltypeStr**, **xltypeMulti**, or **xltypeRef**.</span></span> <span data-ttu-id="a8221-117">Es ist immer sicher, andere Typen frei zu machen, auch wenn sie keinen Zusätzlichen Speicher verwenden, solange Sie sie von **Excel4** oder **Excel12 erhalten haben.**</span><span class="sxs-lookup"><span data-stu-id="a8221-117">It is always safe to free other types even if they do not use auxiliary memory, as long as you got them from **Excel4** or **Excel12**.</span></span>
  
<span data-ttu-id="a8221-118">Wenn Sie zu Excel einem Zeiger auf einen **XLOPER** /  **XLOPER12** zurückkehren, der weiterhin Excel zugewiesenen Arbeitsspeicher enthält, müssen Sie **xlbitXLFree** festlegen, um sicherzustellen, dass Excel den Arbeitsspeicher freilässt.</span><span class="sxs-lookup"><span data-stu-id="a8221-118">Where you are returning to Excel a pointer to an **XLOPER**/ **XLOPER12** that still contains Excel-allocated memory to be freed, you must set the **xlbitXLFree** to ensure Excel releases the memory.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a8221-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a8221-119">Example</span></span>

<span data-ttu-id="a8221-120">In diesem Beispiel wird **GET aufruft. WORKSPACE(1),** um die Plattform zurück, auf der Excel derzeit als Zeichenfolge ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8221-120">This example calls **GET.WORKSPACE(1)** to return the platform on which Excel is currently running as a string.</span></span> <span data-ttu-id="a8221-121">Der Code kopiert diese zurückgegebene Zeichenfolge in einen Puffer für eine spätere Verwendung.</span><span class="sxs-lookup"><span data-stu-id="a8221-121">The code copies this returned string into a buffer for later use.</span></span> <span data-ttu-id="a8221-122">Der Code platziert den Puffer zur späteren Verwendung mit der Excel **xlOPER12.**</span><span class="sxs-lookup"><span data-stu-id="a8221-122">The code places the buffer back into the **XLOPER12** for later use with the Excel function.</span></span> <span data-ttu-id="a8221-123">Schließlich zeigt der Code die Zeichenfolge in einem Warnungsfeld an.</span><span class="sxs-lookup"><span data-stu-id="a8221-123">Finally, the code displays the string in an alert box.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="a8221-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8221-124">See also</span></span>

- [<span data-ttu-id="a8221-125">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="a8221-125">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

