---
title: XlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- XlAutoFree-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a2d2b8e60b484ba8156acc80d543493e3ec9c564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790590"
---
# <a name="xlautofreexlautofree12"></a><span data-ttu-id="3d98d-104">XlAutoFree/xlAutoFree12</span><span class="sxs-lookup"><span data-stu-id="3d98d-104">xlAutoFree/xlAutoFree12</span></span>

 <span data-ttu-id="3d98d-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3d98d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3d98d-106">Wird von Microsoft Excel aufgerufen, nachdem eine XLL-Arbeitsblattfunktion einen **XLOPER**gibt/ **XLOPER12** darauf mit Kennzeichen, die angeben, Arbeitsspeicher, die die XLL weiterhin freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="3d98d-106">Called by Microsoft Excel just after an XLL worksheet function returns an **XLOPER**/ **XLOPER12** to it with a flag set that tells it there is memory that the XLL still needs to release.</span></span> <span data-ttu-id="3d98d-107">Auf diese Weise können die XLL zurückzugebenden dynamisch Arrays, Zeichenfolgen und externe Verweise auf das Arbeitsblatt ohne Speicherverluste zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3d98d-107">This enables the XLL to return dynamically allocated arrays, strings, and external references to the worksheet without memory leaks.</span></span> <span data-ttu-id="3d98d-108">Weitere Informationen finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="3d98d-108">For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="3d98d-109">Ab Excel 2007 werden die **xlAutoFree12** -Funktion und den Datentyp **XLOPER12** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3d98d-109">Starting in Excel 2007, the **xlAutoFree12** function and the **XLOPER12** data type are supported.</span></span> 
  
<span data-ttu-id="3d98d-110">Excel erforderlich keine XLL zu implementieren und exportieren Sie eine dieser Funktionen.</span><span class="sxs-lookup"><span data-stu-id="3d98d-110">Excel does not require an XLL to implement and export either of these functions.</span></span> <span data-ttu-id="3d98d-111">Allerdings müssen Sie dies tun, wenn XLL-Funktionen einer XLOPER oder XLOPER12, die dynamisch zugewiesen oder enthält Verweise auf dynamisch reservierter Speicher, zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="3d98d-111">However, you must do so if your XLL functions return an XLOPER or XLOPER12 that has been dynamically allocated or that contains pointers to dynamically allocated memory.</span></span> <span data-ttu-id="3d98d-112">Stellen Sie sicher, dass Ihrer Wahl zum Verwalten von Arbeitsspeicher für diese Typen konsistent in der gesamten Ihrer XLL und wie Sie **XlAutoFree** und **xlAutoFree12**implementiert.</span><span class="sxs-lookup"><span data-stu-id="3d98d-112">Ensure that your choice of how to manage memory for these types is consistent throughout your XLL and with how you implemented **xlAutoFree** and **xlAutoFree12**.</span></span>
  
<span data-ttu-id="3d98d-113">Innerhalb der **XlAutoFree**/ **xlAutoFree12** -Funktion, Rückrufe in Excel deaktiviert sind, mit einer Ausnahme: **XlFree** aufgerufen werden kann, um Excel reservierten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="3d98d-113">Inside the **xlAutoFree**/ **xlAutoFree12** function, callbacks into Excel are disabled, with one exception: **xlFree** can be called to free Excel-allocated memory.</span></span> 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a><span data-ttu-id="3d98d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d98d-114">Parameters</span></span>

 <span data-ttu-id="3d98d-115">_pxFree_ (**Im Fall von XlAutoFree LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="3d98d-115">_pxFree_ (**LPXLOPER in the case of xlAutoFree**)</span></span>
  
 <span data-ttu-id="3d98d-116">_pxFree_ (**Im Fall von xlAutoFree12 LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="3d98d-116">_pxFree_ (**LPXLOPER12 in the case of xlAutoFree12**)</span></span>
  
<span data-ttu-id="3d98d-117">Ein Zeiger auf die **XLOPER** oder **XLOPER12** mit Arbeitsspeicher, der freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="3d98d-117">A pointer to the **XLOPER** or the **XLOPER12** that has memory that needs to be freed.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="3d98d-118">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d98d-118">Property value/Return value</span></span>

<span data-ttu-id="3d98d-119">Diese Funktion nicht Rückgabewert und sollten als zurückgeben nichtig deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="3d98d-119">This function does not return a value and should be declared as returning void.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3d98d-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3d98d-120">Remarks</span></span>

<span data-ttu-id="3d98d-121">Wenn Excel multithreaded Arbeitsmappe neu berechnen, **XlAutoFree**verwenden konfiguriert ist/ **xlAutoFree12** wird aufgerufen, auf dem gleichen Thread verwendet, um die Funktion aufgerufen wird, die es zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3d98d-121">When Excel is configured to use multithreaded workbook recalculation, **xlAutoFree**/ **xlAutoFree12** is called on the same thread used to call the function that returned it.</span></span> <span data-ttu-id="3d98d-122">Der Aufruf von **XlAutoFree**/ **xlAutoFree12** wird immer durchgeführt werden, bevor alle nachfolgenden Arbeitsblattzellen auf diesem Thread ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="3d98d-122">The call to **xlAutoFree**/ **xlAutoFree12** is always made before any subsequent worksheet cells are evaluated on that thread.</span></span> <span data-ttu-id="3d98d-123">Dies vereinfacht die threadsicheren Design in Ihrer XLL.</span><span class="sxs-lookup"><span data-stu-id="3d98d-123">This simplifies thread-safe design in your XLL.</span></span> 
  
<span data-ttu-id="3d98d-124">Wenn die **XlAutoFree**/ **xlAutoFree12** -Funktion, die Sie bereitstellen beschreibt das Feld **Xltype** _PxFree_, denken Sie daran, dass immer noch das **XlbitDLLFree** Bit festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3d98d-124">If the **xlAutoFree**/ **xlAutoFree12** function you provide looks at the **xltype** field of  _pxFree_, remember that the **xlbitDLLFree** bit will still be set.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3d98d-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3d98d-125">Example</span></span>

 <span data-ttu-id="3d98d-126">**Beispielhafte 1**</span><span class="sxs-lookup"><span data-stu-id="3d98d-126">**Example Implementation 1**</span></span>
  
<span data-ttu-id="3d98d-127">Im ersten Codebeispiel aus `\SAMPLES\EXAMPLE\EXAMPLE.C` veranschaulicht eine ganz bestimmte Implementierung der **XlAutoFree**, zum Arbeiten mit nur einer Funktion, **fArray**vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="3d98d-127">The first code from  `\SAMPLES\EXAMPLE\EXAMPLE.C` demonstrates a very specific implementation of **xlAutoFree**, which is designed to work with just one function, **fArray**.</span></span> <span data-ttu-id="3d98d-128">Im Allgemeinen Ihrer XLL müssen mehrere Funktion zurückgeben von Arbeitsspeicher, der freigegeben werden muss, eine weniger strengen Implementierung ist in diesem Fall erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3d98d-128">In general, your XLL will have more than just one function returning memory that needs to be freed, in which case a less restricted implementation is required.</span></span> 
  
 <span data-ttu-id="3d98d-129">**Beispielhafte 2**</span><span class="sxs-lookup"><span data-stu-id="3d98d-129">**Example implementation 2**</span></span>
  
<span data-ttu-id="3d98d-130">Die zweite Beispiel-Implementierung ist dabei konsistent mit die Annahmen **XLOPER12** Erstellung Beispiele im Abschnitt 1.6.3, xl12_Str_example, xl12_Ref_example und xl12_Multi_example verwendet.</span><span class="sxs-lookup"><span data-stu-id="3d98d-130">The second example implementation is consistent with the assumptions used in the **XLOPER12** creation examples in section 1.6.3, xl12_Str_example, xl12_Ref_example, and xl12_Multi_example.</span></span> <span data-ttu-id="3d98d-131">Die Annahmen sind an, wenn das Bit **XlbitDLLFree** Set, alle String, Array wurde und externer Bezug Arbeitsspeicher dynamisch zugeordnet wurde mit **Malloc**und daher im Gespräch frei freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="3d98d-131">The assumptions are that, when the **xlbitDLLFree** bit has been set, all string, array, and external reference memory has been dynamically allocated using **malloc**, and so needs to be freed in a call to free.</span></span>
  
 <span data-ttu-id="3d98d-132">**Beispielhafte 3**</span><span class="sxs-lookup"><span data-stu-id="3d98d-132">**Example implementation 3**</span></span>
  
<span data-ttu-id="3d98d-133">Die dritte Beispiel-Implementierung ist konsistent mit einer XLL, wo exportierte Funktionen, die **XLOPER12**s zurückgeben Zeichenfolgen, externe Verweise und Arrays mit **Malloc**reservieren und **XLOPER12** selbst auch dynamisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3d98d-133">The third example implementation is consistent with an XLL where exported functions that return **XLOPER12**s allocate strings, external references and arrays using **malloc**, and where the **XLOPER12** itself is also dynamically allocated.</span></span> <span data-ttu-id="3d98d-134">Einen Zeiger auf eine dynamisch zugeordnete zurückgeben ist **XLOPER12** eine Möglichkeit, stellen Sie sicher, dass die Funktion threadsicheren ist.</span><span class="sxs-lookup"><span data-stu-id="3d98d-134">Returning a pointer to a dynamically allocated **XLOPER12** is one way to ensure that the function is thread safe.</span></span> 
  
```cs
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 1
//////////////////////////////////////////
LPXLOPER12 WINAPI fArray(void)
{
    LPXLOPER12 pxArray;
    static XLOPER12 xMulti;
    int i;
    int rwcol;
    xMulti.xltype = xltypeMulti | xlbitDLLFree;
    xMulti.val.array.columns = 1;
    xMulti.val.array.rows = 8;
    // For large values of rows and columns, this would overflow
    // use __int64 in that case and return an error if rwcol
    // contains a number that won't fit in sizeof(int) bytes
    rwcol = xMulti.val.array.columns * xMulti.val.array.rows; 
    pxArray = (LPXLOPER12)GlobalLock(hArray = GlobalAlloc(GMEM_ZEROINIT, rwcol * sizeof(XLOPER12)));
    xMulti.val.array.lparray = pxArray;
    for(i = 0; i < rwcol; i++) 
    {
        pxArray[i].xltype = xltypeInt;
        pxArray[i].val.w = i;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe, use alternate memory allocation mechanisms
    return (LPXLOPER12)&xMulti;
}
void WINAPI xlAutoFree12(LPXLOPER12 pxFree)
{
    GlobalUnlock(hArray);
    GlobalFree(hArray);
    return;
}
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 2
//////////////////////////////////////////
void WINAPI xlAutoFree12(LPXLOPER12 pxFree)
{
    if(pxFree->xltype & xltypeMulti)
    {
/* Assume all string elements were allocated using malloc, and
** need to be freed using free.  Then free the array itself.
*/
        int size = pxFree->val.array.rows *
            pxFree->val.array.columns;
        LPXLOPER12 p = pxFree->val.array.lparray;
        for(; size-- > 0; p++) // check elements for strings
            if(p->xltype == xltypeStr)
                free(p->val.str);
        free(pxFree->val.array.lparray);
    }
    else if(pxFree->xltype & xltypeStr)
    {
        free(pxFree->val.str);
    }
    else if(pxFree->xltype & xltypeRef)
    {
        free(pxFree->val.mref.lpmref);
    }
}
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 3
//////////////////////////////////////////
LPXLOPER12 WINAPI example_xll_function(LPXLOPER12 pxArg)
{
// Thread-safe return value. Every invocation of this function
// gets its own piece of memory.
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
// Initialize to a safe default
    pxRtnValue->xltype = xltypeNil;
// Set the value of pxRtnValue making sure that strings, external
// references, arrays, and strings within arrays are all dynamically
// allocated using malloc.
//    (code omitted)
//    ...
// Set xlbitDLLFree regardless of the type of the return value to
// ensure xlAutoFree12 is called and pxRtnValue is freed.
    pxRtnValue->xltype |= xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER pxFree)
{
    if(pxFree->xltype & xltypeMulti)
    {
// Assume all string elements were allocated using malloc, and
// need to be freed using free. Then free the array itself.
        int size = pxFree->val.array.rows *
            pxFree->val.array.columns;
        LPXLOPER12 p = pxFree->val.array.lparray;
        for(; size-- > 0; p++) // check elements for strings
            if(p->xltype == xltypeStr)
                free(p->val.str);
        free(pxFree->val.array.lparray);
    }
    else if(pxFree->xltype & xltypeStr)
    {
        free(pxFree->val.str);
    }
    else if(pxFree->xltype & xltypeRef)
    {
        free(pxFree->val.mref.lpmref);
    }
// Assume pxFree was itself dynamically allocated using malloc.
    free(pxFree);
}
```

## <a name="see-also"></a><span data-ttu-id="3d98d-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d98d-135">See also</span></span>



[<span data-ttu-id="3d98d-136">Add-In-Manager und Funktionen von XLL-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3d98d-136">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

