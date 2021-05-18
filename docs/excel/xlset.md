---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- xlset-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0912c1d40882933778d0df927ceb9de773063444
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404603"
---
# <a name="xlset"></a>xlSet

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Legt konstante Werte sehr schnell in Zellen oder Bereiche. Weitere Informationen finden Sie unter "xlSet and Workbooks with Array Formulas" [unter Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a>Parameter

_pxReference_ (**xltypeRef** oder **xltypeSRef**)
  
Ein rechteckiger Verweis, der die Zielzelle oder -zellen beschreibt. Der Verweis muss benachbarte Zellen beschreiben, sodass in **einem xltypeRef** `val.mref.lpmref->count` auf 1 festgelegt werden muss. 
  
_pxValue_
  
Der Wert oder die Werte, die in die Zelle oder Zellen platziert werden sollen. Weitere Informationen finden Sie im Abschnitt "Hinweise".
  
## <a name="remarks"></a>Hinweise

### <a name="pxvalue-argument"></a>pxValue-Argument

_pxValue_ kann entweder ein Wert oder ein Array sein. Wenn es sich um einen Wert handelt, wird der gesamte Zielbereich mit diesem Wert gefüllt. Wenn es sich um ein Array (**xltypeMulti)** handelt, werden die Elemente des Arrays an die entsprechenden Speicherorte im Rechteck eingesenert.
  
Wenn Sie ein horizontales Array für das zweite Argument verwenden, wird es nach unten dupliziert, um das gesamte Rechteck zu füllen. Wenn Sie ein vertikales Array verwenden, wird es nach rechts dupliziert, um das gesamte Rechteck zu füllen. Wenn Sie ein rechteckiges Array verwenden und es zu klein für den rechteckigen Bereich ist, in den Sie es setzen möchten, wird dieser Bereich mit **#N/A-s gepolstert.**
  
Wenn der Zielbereich kleiner als das Quellarray ist, werden die Werte bis zu den Grenzen des Zielbereichs kopiert, und die zusätzlichen Daten werden ignoriert.
  
Verwenden Sie ein **xltypeNil-Arrayelement** im Quellarray, um ein Element des Zielrechtecks zu löschen. Um das gesamte Zielrechteck zu löschen, lassen Sie das zweite Argument aus. 
  
### <a name="restrictions"></a>Einschränkungen

**xlSet** kann nicht rückgängig gemacht werden. Darüber hinaus werden alle Zuvor verfügbaren Rückgängig-Informationen vernichtet. 
  
**xlSet** kann nur Konstanten, nicht Formeln, in Zellen setzen. 
  
**xlSet** verhält sich wie eine Befehlsentsprechungsfunktion der Klasse 3. Das heißt, sie ist nur innerhalb einer DLL verfügbar, wenn die DLL über ein  Objekt, ein Makro, ein Menü, eine Symbolleiste, eine Tastenkombination oder die Schaltfläche Ausführen im Dialogfeld **Makro** aufgerufen wird (zugriff auf die Registerkarte Ansicht auf dem Menüband ab Excel 2007 und das Menü **Extras** in früheren Versionen).  
  
## <a name="example"></a>Beispiel

Das folgende Beispiel füllt B205:B206 mit dem Wert aus, der von einem Makro übergeben wurde. Dieses Befehlsfunktionsbeispiel erfordert ein Argument und funktioniert nur, wenn es von einem XLM-Makroblatt oder von einem VBA-Modul mit der **Application.Run-Methode aufgerufen** wird. 
  
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

