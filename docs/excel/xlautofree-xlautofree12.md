---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- xlautofree-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3dfba5ae98b0635c95308eac01bf2f10867678e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413290"
---
# <a name="xlautofreexlautofree12"></a><span data-ttu-id="a5111-104">xlAutoFree/xlAutoFree12</span><span class="sxs-lookup"><span data-stu-id="a5111-104">xlAutoFree/xlAutoFree12</span></span>

 <span data-ttu-id="a5111-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a5111-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a5111-106">Wird von Microsoft Excel direkt nach einer XLL-Arbeitsblattfunktion aufgerufen, wird ein **XLOPER** /  **XLOPER12-Wert** mit einem Flagsatz zurückgegeben, der angibt, dass der Speicher vorhanden ist, den die XLL noch losgibt.</span><span class="sxs-lookup"><span data-stu-id="a5111-106">Called by Microsoft Excel just after an XLL worksheet function returns an **XLOPER**/ **XLOPER12** to it with a flag set that tells it there is memory that the XLL still needs to release.</span></span> <span data-ttu-id="a5111-107">Dadurch kann die XLL dynamisch zugewiesene Arrays, Zeichenfolgen und externe Verweise auf das Arbeitsblatt ohne Speicherverluste zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a5111-107">This enables the XLL to return dynamically allocated arrays, strings, and external references to the worksheet without memory leaks.</span></span> <span data-ttu-id="a5111-108">Weitere Informationen finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="a5111-108">For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="a5111-109">Ab Excel 2007 werden die **xlAutoFree12-Funktion** und der **XLOPER12-Datentyp** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a5111-109">Starting in Excel 2007, the **xlAutoFree12** function and the **XLOPER12** data type are supported.</span></span> 
  
<span data-ttu-id="a5111-110">Excel erfordert keine XLL zum Implementieren und Exportieren einer dieser Funktionen.</span><span class="sxs-lookup"><span data-stu-id="a5111-110">Excel does not require an XLL to implement and export either of these functions.</span></span> <span data-ttu-id="a5111-111">Sie müssen dies jedoch tun, wenn Ihre XLL-Funktionen einen XLOPER- oder XLOPER12-Wert zurückgeben, der dynamisch zugewiesen wurde oder Zeiger auf dynamisch zugewiesenen Arbeitsspeicher enthält.</span><span class="sxs-lookup"><span data-stu-id="a5111-111">However, you must do so if your XLL functions return an XLOPER or XLOPER12 that has been dynamically allocated or that contains pointers to dynamically allocated memory.</span></span> <span data-ttu-id="a5111-112">Stellen Sie sicher, dass Die Wahl der Verwaltung des Arbeitsspeichers für diese Typen in Ihrer gesamten XLL und mit der Implementierung von **xlAutoFree** und **xlAutoFree12 konsistent ist.**</span><span class="sxs-lookup"><span data-stu-id="a5111-112">Ensure that your choice of how to manage memory for these types is consistent throughout your XLL and with how you implemented **xlAutoFree** and **xlAutoFree12**.</span></span>
  
<span data-ttu-id="a5111-113">Innerhalb der **xlAutoFree** /  **xlAutoFree12-Funktion** sind Rückrufe in Excel deaktiviert, mit einer Ausnahme: **xlFree** kann aufgerufen werden, um Excel zugewiesenen Arbeitsspeicher frei zu geben.</span><span class="sxs-lookup"><span data-stu-id="a5111-113">Inside the **xlAutoFree**/ **xlAutoFree12** function, callbacks into Excel are disabled, with one exception: **xlFree** can be called to free Excel-allocated memory.</span></span> 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a><span data-ttu-id="a5111-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5111-114">Parameters</span></span>

 <span data-ttu-id="a5111-115">_pxFree_ (**LPXLOPER im Fall von xlAutoFree**)</span><span class="sxs-lookup"><span data-stu-id="a5111-115">_pxFree_ (**LPXLOPER in the case of xlAutoFree**)</span></span>
  
 <span data-ttu-id="a5111-116">_pxFree_ (**LPXLOPER12 im Fall von xlAutoFree12**)</span><span class="sxs-lookup"><span data-stu-id="a5111-116">_pxFree_ (**LPXLOPER12 in the case of xlAutoFree12**)</span></span>
  
<span data-ttu-id="a5111-117">Ein Zeiger auf **xlOPER** oder **XLOPER12,** der über Arbeitsspeicher verfügt, der frei werden muss.</span><span class="sxs-lookup"><span data-stu-id="a5111-117">A pointer to the **XLOPER** or the **XLOPER12** that has memory that needs to be freed.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a5111-118">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5111-118">Property value/Return value</span></span>

<span data-ttu-id="a5111-119">Diese Funktion gibt keinen Wert zurück und sollte als void deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="a5111-119">This function does not return a value and should be declared as returning void.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a5111-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a5111-120">Remarks</span></span>

<span data-ttu-id="a5111-121">Wenn Excel für die Verwendung der Neuberechnung von Arbeitsmappen mit mehrerenReads konfiguriert ist, wird **xlAutoFree** /  **xlAutoFree12** für denselben Thread aufgerufen, der zum Aufrufen der Zurückgegebenen Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a5111-121">When Excel is configured to use multithreaded workbook recalculation, **xlAutoFree**/ **xlAutoFree12** is called on the same thread used to call the function that returned it.</span></span> <span data-ttu-id="a5111-122">Der Aufruf von **xlAutoFree**/ **xlAutoFree12** erfolgt immer vor der Auswertung aller nachfolgenden Arbeitsblattzellen in diesem Thread.</span><span class="sxs-lookup"><span data-stu-id="a5111-122">The call to **xlAutoFree**/ **xlAutoFree12** is always made before any subsequent worksheet cells are evaluated on that thread.</span></span> <span data-ttu-id="a5111-123">Dies vereinfacht das threadsichere Design in Ihrer XLL.</span><span class="sxs-lookup"><span data-stu-id="a5111-123">This simplifies thread-safe design in your XLL.</span></span> 
  
<span data-ttu-id="a5111-124">Wenn die **xlAutoFree** /  **xlAutoFree12-Funktion,** die Sie bereitstellen, das **xltype-Feld** _von pxFree_ betrachtet, denken Sie daran, dass das **xlbitDLLFree-Bit** weiterhin festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a5111-124">If the **xlAutoFree**/ **xlAutoFree12** function you provide looks at the **xltype** field of  _pxFree_, remember that the **xlbitDLLFree** bit will still be set.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a5111-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a5111-125">Example</span></span>

 <span data-ttu-id="a5111-126">**Beispielimplementierung 1**</span><span class="sxs-lookup"><span data-stu-id="a5111-126">**Example Implementation 1**</span></span>
  
<span data-ttu-id="a5111-127">Der erste Code aus veranschaulicht eine sehr spezifische Implementierung von xlAutoFree , die mit nur einer `\SAMPLES\EXAMPLE\EXAMPLE.C` Funktion, **fArray**, funktioniert. </span><span class="sxs-lookup"><span data-stu-id="a5111-127">The first code from  `\SAMPLES\EXAMPLE\EXAMPLE.C` demonstrates a very specific implementation of **xlAutoFree**, which is designed to work with just one function, **fArray**.</span></span> <span data-ttu-id="a5111-128">Im Allgemeinen hat Ihre XLL mehr als nur eine Funktion, die Arbeitsspeicher zurück gibt, der frei werden muss, in diesem Fall ist eine weniger eingeschränkte Implementierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a5111-128">In general, your XLL will have more than just one function returning memory that needs to be freed, in which case a less restricted implementation is required.</span></span> 
  
 <span data-ttu-id="a5111-129">**Beispielimplementierung 2**</span><span class="sxs-lookup"><span data-stu-id="a5111-129">**Example implementation 2**</span></span>
  
<span data-ttu-id="a5111-130">Die zweite Beispielimplementierung entspricht den Annahmen in den **XLOPER12-Erstellungsbeispielen** in Abschnitt 1.6.3, xl12_Str_example, xl12_Ref_example und xl12_Multi_example.</span><span class="sxs-lookup"><span data-stu-id="a5111-130">The second example implementation is consistent with the assumptions used in the **XLOPER12** creation examples in section 1.6.3, xl12_Str_example, xl12_Ref_example, and xl12_Multi_example.</span></span> <span data-ttu-id="a5111-131">Es wird davon ausgegangen, dass, wenn das **xlbitDLLFree-Bit** festgelegt wurde, der ganze Zeichenfolgen-, Array- und externer Referenzspeicher mithilfe von **malloc** dynamisch zugewiesen wurde und daher in einem Aufruf zur Kostenlosen Verwendung frei werden muss.</span><span class="sxs-lookup"><span data-stu-id="a5111-131">The assumptions are that, when the **xlbitDLLFree** bit has been set, all string, array, and external reference memory has been dynamically allocated using **malloc**, and so needs to be freed in a call to free.</span></span>
  
 <span data-ttu-id="a5111-132">**Beispielimplementierung 3**</span><span class="sxs-lookup"><span data-stu-id="a5111-132">**Example implementation 3**</span></span>
  
<span data-ttu-id="a5111-133">Die dritte Beispielimplementierung ist mit einer XLL konsistent, bei der exportierte Funktionen, die **XLOPER12** s zurückgeben, Zeichenfolgen, externe Verweise und Arrays mithilfe von **malloc** zuordnen und wobei **xlOPER12** selbst ebenfalls dynamisch zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="a5111-133">The third example implementation is consistent with an XLL where exported functions that return **XLOPER12** s allocate strings, external references and arrays using **malloc**, and where the **XLOPER12** itself is also dynamically allocated.</span></span> <span data-ttu-id="a5111-134">Das Zurückgeben eines Zeigers auf eine dynamisch zugewiesene **XLOPER12** ist eine Möglichkeit, um sicherzustellen, dass die Funktion threadsicher ist.</span><span class="sxs-lookup"><span data-stu-id="a5111-134">Returning a pointer to a dynamically allocated **XLOPER12** is one way to ensure that the function is thread safe.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="a5111-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5111-135">See also</span></span>



[<span data-ttu-id="a5111-136">Add-In-Manager und XLL-Benutzeroberflächenfunktionen</span><span class="sxs-lookup"><span data-stu-id="a5111-136">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

