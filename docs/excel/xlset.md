---
title: gleich xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- gleich XlSet-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 63f50e441f5d851677f36754a17bcd6403705239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790624"
---
# <a name="xlset"></a>gleich xlSet

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Konstantenwerte versetzt sehr schnell in Zellen oder Bereichen. Weitere Informationen finden Sie unter "gleich XlSet und Arbeitsmappen mit Arrayformeln" unter [Bekannte Probleme bei der Entwicklung von Excel XLL](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a>Parameter

_pxReference_ (**XltypeRef** oder **XltypeSRef**)
  
Einen rechteckigen Verweis zur Beschreibung des Zielzelle oder Zellen. Der Verweis muss also angrenzende Zellen beschreiben, die in einer **XltypeRef** `val.mref.lpmref->count` muss auf 1 festgelegt werden. 
  
_pxValue_
  
Der Wert oder die Werte in die Zelle oder die Zellen eingefügt werden. Weitere Informationen finden Sie im Abschnitt "Hinweise".
  
## <a name="remarks"></a>Hinweise

### <a name="pxvalue-argument"></a>PxValue-argument

_PxValue_ kann entweder ein Wert oder ein Array sein. Wenn sie ein Wert ist, wird mit diesem Wert der gesamten Zielbereich gefüllt. Wenn es sich um ein Array (**XltypeMulti**) ist, werden die Elemente des Arrays in die entsprechenden Speicherorte im Rechteck eingefügt.
  
Wenn Sie ein horizontales Array für das zweite Argument verwenden, wird es nach unten dupliziert, um das gesamte Rechteck zu füllen. Wenn Sie ein vertikales Array verwenden, wird er dupliziert rechts, um das gesamte Rechteck zu füllen. Wenn Sie ein rechteckiges Array verwenden, und es ist zu klein für den rechteckigen Bereich, den Sie ihn in aufnehmen möchten, wird dieses Bereichs mit **#n/a**s aufgefüllt.
  
Wenn der Zielbereich kleiner als das Quell-Array ist, die Werte werden den Grenzen der Zielbereich kopiert und die zusätzlichen Daten werden ignoriert.
  
Ein Element des Zielrechtecks verwenden, um ein **XltypeNil** Typ Arrayelement im Quell-Array. Deaktivieren Sie das gesamte Zielrechteck, ausgelassen werden Sie, das zweite Argument. 
  
### <a name="restrictions"></a>Einschränkungen

**gleich XlSet** kann nicht rückgängig gemacht werden. Darüber hinaus werden sie alle Rückgängig-Informationen, die vor dem verfügbaren möglicherweise wurden. 
  
**gleich XlSet** können nur Konstanten, nicht Formeln in Zellen einfügen. 
  
**gleich XlSet** verhält sich wie eine Klasse 3 Befehl äquivalente Funktion; d. h., steht er nur innerhalb einer DLL die DLL aufgerufen wird, ein Objekt, Makro, Menü, Symbolleiste, Tastenkombination oder die Schaltfläche **Ausführen** im Dialogfeld **Makro** (Zugriff über die Registerkarte **Ansicht** auf dem Menüband in Excel 2007 und den Tools **Starten **Menü in früheren Versionen). 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird die B205:B206 mit dem Wert, der aus einem Makro übergeben wurde. In diesem Befehlsbeispiel-Funktion erfordert ein Argument, und so funktioniert nur, wenn Sie aus einer XLM-Makrovorlage oder aus einem VBA-Modul die **entsprechende** -Methode aufgerufen wird. 
  
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
- [C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

