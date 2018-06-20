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
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a2d2b8e60b484ba8156acc80d543493e3ec9c564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790590"
---
# <a name="xlautofreexlautofree12"></a>XlAutoFree/xlAutoFree12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird von Microsoft Excel aufgerufen, nachdem eine XLL-Arbeitsblattfunktion einen **XLOPER**gibt/ **XLOPER12** darauf mit Kennzeichen, die angeben, Arbeitsspeicher, die die XLL weiterhin freigegeben werden muss. Auf diese Weise können die XLL zurückzugebenden dynamisch Arrays, Zeichenfolgen und externe Verweise auf das Arbeitsblatt ohne Speicherverluste zugewiesen. Weitere Informationen finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).
  
Ab Excel 2007 werden die **xlAutoFree12** -Funktion und den Datentyp **XLOPER12** unterstützt. 
  
Excel erforderlich keine XLL zu implementieren und exportieren Sie eine dieser Funktionen. Allerdings müssen Sie dies tun, wenn XLL-Funktionen einer XLOPER oder XLOPER12, die dynamisch zugewiesen oder enthält Verweise auf dynamisch reservierter Speicher, zurückzugeben. Stellen Sie sicher, dass Ihrer Wahl zum Verwalten von Arbeitsspeicher für diese Typen konsistent in der gesamten Ihrer XLL und wie Sie **XlAutoFree** und **xlAutoFree12**implementiert.
  
Innerhalb der **XlAutoFree**/ **xlAutoFree12** -Funktion, Rückrufe in Excel deaktiviert sind, mit einer Ausnahme: **XlFree** aufgerufen werden kann, um Excel reservierten Arbeitsspeicher freizugeben. 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a>Parameter

 _pxFree_ (**Im Fall von XlAutoFree LPXLOPER**)
  
 _pxFree_ (**Im Fall von xlAutoFree12 LPXLOPER12**)
  
Ein Zeiger auf die **XLOPER** oder **XLOPER12** mit Arbeitsspeicher, der freigegeben werden muss. 
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Diese Funktion nicht Rückgabewert und sollten als zurückgeben nichtig deklariert werden.
  
## <a name="remarks"></a>Hinweise

Wenn Excel multithreaded Arbeitsmappe neu berechnen, **XlAutoFree**verwenden konfiguriert ist/ **xlAutoFree12** wird aufgerufen, auf dem gleichen Thread verwendet, um die Funktion aufgerufen wird, die es zurückgegeben. Der Aufruf von **XlAutoFree**/ **xlAutoFree12** wird immer durchgeführt werden, bevor alle nachfolgenden Arbeitsblattzellen auf diesem Thread ausgewertet werden. Dies vereinfacht die threadsicheren Design in Ihrer XLL. 
  
Wenn die **XlAutoFree**/ **xlAutoFree12** -Funktion, die Sie bereitstellen beschreibt das Feld **Xltype** _PxFree_, denken Sie daran, dass immer noch das **XlbitDLLFree** Bit festgelegt wird. 
  
## <a name="example"></a>Beispiel

 **Beispielhafte 1**
  
Im ersten Codebeispiel aus `\SAMPLES\EXAMPLE\EXAMPLE.C` veranschaulicht eine ganz bestimmte Implementierung der **XlAutoFree**, zum Arbeiten mit nur einer Funktion, **fArray**vorgesehen ist. Im Allgemeinen Ihrer XLL müssen mehrere Funktion zurückgeben von Arbeitsspeicher, der freigegeben werden muss, eine weniger strengen Implementierung ist in diesem Fall erforderlich. 
  
 **Beispielhafte 2**
  
Die zweite Beispiel-Implementierung ist dabei konsistent mit die Annahmen **XLOPER12** Erstellung Beispiele im Abschnitt 1.6.3, xl12_Str_example, xl12_Ref_example und xl12_Multi_example verwendet. Die Annahmen sind an, wenn das Bit **XlbitDLLFree** Set, alle String, Array wurde und externer Bezug Arbeitsspeicher dynamisch zugeordnet wurde mit **Malloc**und daher im Gespräch frei freigegeben werden muss.
  
 **Beispielhafte 3**
  
Die dritte Beispiel-Implementierung ist konsistent mit einer XLL, wo exportierte Funktionen, die **XLOPER12**s zurückgeben Zeichenfolgen, externe Verweise und Arrays mit **Malloc**reservieren und **XLOPER12** selbst auch dynamisch zugewiesen wird. Einen Zeiger auf eine dynamisch zugeordnete zurückgeben ist **XLOPER12** eine Möglichkeit, stellen Sie sicher, dass die Funktion threadsicheren ist. 
  
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

## <a name="see-also"></a>Siehe auch



[Add-In-Manager und Funktionen von XLL-Schnittstelle](add-in-manager-and-xll-interface-functions.md)

