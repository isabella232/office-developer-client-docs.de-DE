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
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2dd61ee5cd0e2e671cc47425689287b8a437732f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790607"
---
# <a name="xlfree"></a><span data-ttu-id="b3fa6-104">xlFree</span><span class="sxs-lookup"><span data-stu-id="b3fa6-104">xlFree</span></span>

 <span data-ttu-id="b3fa6-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b3fa6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b3fa6-106">Verwendet, um Ressourcen, die von Microsoft Excel beim Erstellen der Rückgabe Wert **XLOPER**Arbeitsspeicher freizugeben/ **XLOPER12** in einem Aufruf von [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)oder [Excel12v](excel4v-excel12v.md).</span><span class="sxs-lookup"><span data-stu-id="b3fa6-106">Used to free memory resources allocated by Microsoft Excel when creating the return value **XLOPER**/ **XLOPER12** in a call to [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), or [Excel12v](excel4v-excel12v.md).</span></span> <span data-ttu-id="b3fa6-107">**XlFree** -Funktion gibt den zusätzlichen Arbeitsspeicher frei und setzt den Zeiger auf **einen Nullwert fest** , jedoch ist nicht Teil der **XLOPER**zerstören/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="b3fa6-107">The **xlFree** function frees the auxiliary memory and resets the pointer to **NULL** but does not destroy other parts of the **XLOPER**/ **XLOPER12**.</span></span>
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a><span data-ttu-id="b3fa6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3fa6-108">Parameters</span></span>

 <span data-ttu-id="b3fa6-109">_px_1,..., px_n_</span><span class="sxs-lookup"><span data-stu-id="b3fa6-109">_px_1, ..., px_n_</span></span>
  
<span data-ttu-id="b3fa6-110">Eine oder mehrere **XLOPER**/ **XLOPER12**s freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b3fa6-110">One or more **XLOPER**/ **XLOPER12**s to be freed.</span></span> <span data-ttu-id="b3fa6-111">In Excel-Versionen bis zu 2003 ist die maximale Anzahl von Zeigern übergeben werden kann, die 30.</span><span class="sxs-lookup"><span data-stu-id="b3fa6-111">In Excel versions up to 2003, the maximum number of pointers that can be passed is 30.</span></span> <span data-ttu-id="b3fa6-112">Ab Excel 2007, wird dies auf 255 erhöht.</span><span class="sxs-lookup"><span data-stu-id="b3fa6-112">Starting in Excel 2007, this is increased to 255.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b3fa6-113">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3fa6-113">Property value/Return value</span></span>

<span data-ttu-id="b3fa6-114">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b3fa6-114">This function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b3fa6-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b3fa6-115">Remarks</span></span>

<span data-ttu-id="b3fa6-116">Sie müssen alle **XLOPER** , die Sie als Rückgabewert von **Excel4** oder **Excel4v** erhalten und jeder **XLOPER12** , die Sie als Rückgabewert aus der **Excel12** oder **Excel12v** abrufen, wenn sie einen der folgenden Typen sind frei: **XltypeStr **, **XltypeMulti**oder **XltypeRef**.</span><span class="sxs-lookup"><span data-stu-id="b3fa6-116">You must free every **XLOPER** that you get as a return value from **Excel4** or **Excel4v** and every **XLOPER12** that you get as a return value from **Excel12** or **Excel12v** if they are one of the following types: **xltypeStr**, **xltypeMulti**, or **xltypeRef**.</span></span> <span data-ttu-id="b3fa6-117">Es ist sicherer, andere Typen freizugeben, auch wenn sie keine zusätzlichen Arbeitsspeicher verwenden, solange Sie diese von **Excel4** oder **Excel12**erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="b3fa6-117">It is always safe to free other types even if they do not use auxiliary memory, as long as you got them from **Excel4** or **Excel12**.</span></span>
  
<span data-ttu-id="b3fa6-118">In dem Sie zurückgeben nach Excel eines Zeigers auf eine **XLOPER**/ **XLOPER12** , das Excel-reservierter Speicher freigegeben werden weiterhin enthält, muss die **XlbitXLFree** Excel-Versionen des Speichers sicherstellen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b3fa6-118">Where you are returning to Excel a pointer to an **XLOPER**/ **XLOPER12** that still contains Excel-allocated memory to be freed, you must set the **xlbitXLFree** to ensure Excel releases the memory.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b3fa6-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b3fa6-119">Example</span></span>

<span data-ttu-id="b3fa6-120">Dieses Beispiel ruft **erhalten möchten. WORKSPACE(1)** die Plattform zurückgegeben, auf welche Excel als Zeichenfolge ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3fa6-120">This example calls **GET.WORKSPACE(1)** to return the platform on which Excel is currently running as a string.</span></span> <span data-ttu-id="b3fa6-121">Diesem zurückgegebenen Zeichenfolge in einen Puffer zur späteren Verwendung kopiert.</span><span class="sxs-lookup"><span data-stu-id="b3fa6-121">The code copies this returned string into a buffer for later use.</span></span> <span data-ttu-id="b3fa6-122">Der Code einfügt den Puffer wieder in **XLOPER12** zur späteren Verwendung mit der Excel-Funktion.</span><span class="sxs-lookup"><span data-stu-id="b3fa6-122">The code places the buffer back into the **XLOPER12** for later use with the Excel function.</span></span> <span data-ttu-id="b3fa6-123">Abschließend zeigt der Code die Zeichenfolge in einer Warnung an.</span><span class="sxs-lookup"><span data-stu-id="b3fa6-123">Finally, the code displays the string in an alert box.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="b3fa6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3fa6-124">See also</span></span>

- [<span data-ttu-id="b3fa6-125">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen</span><span class="sxs-lookup"><span data-stu-id="b3fa6-125">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

