---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- Xlset-Funktion [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a99d904c4aa9845146ffe2d05dff45859de3b434
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576604"
---
# <a name="xlset"></a>xlSet

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Legt konstanten Werte sehr schnell in Zellen oder Bereiche. Weitere Informationen finden Sie unter "xlSet and Workbooks with Array Formulas" in [Known Issues in Excel XLL Development.](known-issues-in-excel-xll-development.md)
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a>Parameter

_pxReference_ (**xltypeRef** oder **xltypeSRef**)
  
Ein rechteckiger Bezug, der die Zielzelle oder -zellen beschreibt. Der Bezug muss angrenzende Zellen beschreiben, damit in einem **XltypeRef** `val.mref.lpmref->count` der Wert 1 festgelegt werden muss. 
  
_pxValue_
  
Der Wert oder die Werte, die in der Zelle oder den Zellen platziert werden sollen. Weitere Informationen finden Sie im Abschnitt "Hinweise".
  
## <a name="remarks"></a>HinwBemerkungeneise

### <a name="pxvalue-argument"></a>pxValue-Argument

_pxValue_ kann entweder ein Wert oder ein Array sein. Wenn es sich um einen Wert handelt, wird der gesamte Zielbereich mit diesem Wert gefüllt. Wenn es sich um ein Array (**xltypeMulti**) handelt, werden die Elemente des Arrays an den entsprechenden Stellen im Rechteck abgelegt.
  
Wenn Sie für das zweite Argument ein horizontales Array verwenden, wird es dupliziert, um das gesamte Rechteck zu füllen. Wenn Sie ein vertikales Array verwenden, wird es rechts dupliziert, um das gesamte Rechteck auszufüllen. Wenn Sie ein rechteckiges Array verwenden und es für den rechteckigen Bereich, in den Sie ihn einfügen möchten, zu klein ist, wird dieser Bereich mit **#N/A** aufgefüllt.
  
Wenn der Zielbereich kleiner als das Quellarray ist, werden die Werte bis zu den Grenzwerten des Zielbereichs kopiert, und die zusätzlichen Daten werden ignoriert.
  
Um ein Element des Zielrechtecks zu löschen, verwenden Sie ein Arrayelement vom Typ **xltypeNil** im Quellarray. Um das gesamte Zielrechteck zu löschen, lassen Sie das zweite Argument aus. 
  
### <a name="restrictions"></a>Einschränkungen

**xlSet** kann nicht rückgängig sein. Darüber hinaus werden alle Rückgängig-Informationen zerstört, die möglicherweise zuvor verfügbar waren. 
  
**XlSet** kann nur Konstanten und keine Formeln in Zellen einfügen. 
  
**xlSet** verhält sich wie eine Befehlsentsprechungsfunktion der Klasse 3; Das heißt, sie ist nur innerhalb einer DLL verfügbar, wenn die DLL über ein Objekt, ein Makro, ein Menü, eine Symbolleiste, eine Tastenkombination oder die Schaltfläche **"Ausführen"** im Dialogfeld **"Makro"** aufgerufen wird (zugriff über die Registerkarte **"Ansicht"** auf dem Menüband ab Excel 2007 und das Menü **"Extras"** in früheren Versionen). 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird B205:B206 mit dem Wert gefüllt, der von einem Makro übergeben wurde. Dieses Befehlsfunktionsbeispiel erfordert ein Argument und funktioniert daher nur, wenn es von einem XLM-Makroblatt oder von einem VBA-Modul mithilfe der **Application.Run-Methode** aufgerufen wird. 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSetExample(short int iVal)
{
   XLOPER12 xRef, xValue;
   xRef.xltype = xltypeSRef;
   xRef.val.sref.count = 1;
   xRef.val.sref.ref.rwFirst = 204;
   xRef.val.sref.ref.rwLast = 205;
   xRef.val.sref.ref.colFirst = 1;
   xRef.val.sref.ref.colLast = 1;
   xValue.xltype = xltypeInt;
   xValue.val.w = iVal;
   Excel12(xlSet, 0, 2, (LPXLOPER12)&xRef, (LPXLOPER12)&xValue);
   return 1;
}
```

## <a name="see-also"></a>Siehe auch

- [xlCoerce](xlcoerce.md)
- [C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

