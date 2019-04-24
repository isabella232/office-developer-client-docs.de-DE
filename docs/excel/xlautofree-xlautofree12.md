---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- xlAutoFree-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3dfba5ae98b0635c95308eac01bf2f10867678e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303969"
---
# <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Aufgerufen von Microsoft Excel direkt nach einer XLL-Arbeitsblattfunktion gibt ein **XLOPER**/ -**XLOPER12** mit einem Flagsatz zurück, der angibt, dass Speicherplatz vorhanden ist, den die XLL noch freigeben muss. Dadurch kann die XLL dynamisch zugewiesene Arrays, Zeichenfolgen und externe Verweise auf das Arbeitsblatt ohne Speicherverluste zurückgeben. Weitere Informationen finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md).
  
Ab Excel 2007 werden die **xlAutoFree12** -Funktion und der **XLOPER12** -Datentyp unterstützt. 
  
Excel erfordert keine XLL zum Implementieren und Exportieren einer dieser Funktionen. Sie müssen dies tun, wenn Ihre XLL-Funktionen eine XLOPER oder XLOPER12 zurückgeben, die dynamisch zugewiesen wurde oder Zeiger auf dynamisch zugewiesenen Arbeitsspeicher enthält. Stellen Sie sicher, dass Ihre Auswahl für die Verwaltung des Arbeitsspeichers für diese Typen in ihrer XLL konsistent ist und wie Sie **xlAutoFree** und **xlAutoFree12**implementiert haben.
  
Innerhalb der **xlAutoFree**/ -**xlAutoFree12** -Funktion sind Rückrufe in Excel deaktiviert, mit einer Ausnahme: **xlFree** kann aufgerufen werden, um in Excel zugewiesene Arbeitsspeicher freizugeben. 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a>Parameter

 _pxFree_ (**LPXLOPER im Fall von xlAutoFree**)
  
 _pxFree_ (**LPXLOPER12 im Fall von xlAutoFree12**)
  
Ein Zeiger auf das **XLOPER** -oder **XLOPER12** -Arbeitsspeicher, der freigegeben werden muss. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Diese Funktion gibt keinen Wert zurück und sollte als zurückgegeben void deklariert werden.
  
## <a name="remarks"></a>Bemerkungen

Wenn Excel für die Neuberechnung der Multithread-Arbeitsmappe konfiguriert ist, wird **xlAutoFree**/ **xlAutoFree12** für den gleichen Thread aufgerufen, der zum Aufrufen der Funktion verwendet wird, die ihn zurückgegeben hat. Der Aufruf von **xlAutoFree**/ **xlAutoFree12** erfolgt immer vor der Auswertung aller nachfolgenden Arbeitsblattzellen in diesem Thread. Dies vereinfacht das threadsichere Design in Ihrer XLL. 
  
Wenn die **xlAutoFree**/ -**xlAutoFree12** -Funktion, die Sie bereitstellen, das **xltype** -Feld von _pxFree_, denken Sie daran, dass das **xlbitDLLFree** -Bit weiterhin festgelegt wird. 
  
## <a name="example"></a>Beispiel

 **Beispielimplementierung 1**
  
Der erste Code aus `\SAMPLES\EXAMPLE\EXAMPLE.C` demonstriert eine sehr spezifische Implementierung von **xlAutoFree**, die nur mit einer einzigen Funktion, **fArray**, ausgeführt werden kann. Im Allgemeinen hat ihre XLL mehr als eine Funktion, die Speicher zurückgibt, die freigegeben werden muss, in diesem Fall ist eine weniger eingeschränkte Implementierung erforderlich. 
  
 **Beispielimplementierung 2**
  
Die zweite Beispielimplementierung entspricht den Annahmen, die in den **XLOPER12** -Erstellungs Beispielen in Abschnitt 1.6.3, Xl12_Str_example, Xl12_Ref_example und xl12_Multi_example verwendet werden. Die Annahmen sind, dass, wenn das **xlbitDLLFree** -Bit festgelegt wurde, alle Zeichenfolge, Array und externe Referenzspeicher dynamisch mit **malloc**zugewiesen wurde, und daher muss in einem Aufruf von Free freigegeben werden.
  
 **Beispielimplementierung 3**
  
Die dritte Beispielimplementierung ist mit einer XLL konsistent, bei der exportierte Funktionen, die **XLOPER12**s-Zeichenfolgen, externe Verweise und Arrays mit **malloc**zurückgeben und die **XLOPER12** selbst dynamisch zugeordnet ist. Das Zurückgeben eines Zeigers auf eine dynamisch zugewiesene **XLOPER12** ist eine Möglichkeit, um sicherzustellen, dass die Funktion threadsicher ist. 
  
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



[Add-In-Manager und XLL-Benutzeroberflächenfunktionen](add-in-manager-and-xll-interface-functions.md)

