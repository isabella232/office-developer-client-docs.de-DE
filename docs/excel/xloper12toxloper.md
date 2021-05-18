---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- xloper12toxloper-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 148353dcec1cc051aa44d18c0a081b6623e3759a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422908"
---
# <a name="xloper12toxloper"></a>XLOper12ToXLOper

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Konvertierungsroutine, die zum Konvertieren von der neuen **XLOPER12 in** die alte **XLOPER verwendet wird.**
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a>Parameter

_pxloper12_ (**LPXLOPER12**)
  
Zeiger auf die zu **konvertierte XlOPER12-Quelle.** 
  
_pxloper_ (**LPXLOPER**)
  
Zeiger auf das **XlOPER-Ziel,** das den konvertierten Wert enthalten soll. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

**TRUE,** wenn die Konvertierung erfolgreich war, **andernfalls FALSE.** 
  
## <a name="remarks"></a>Hinweise

Je nach Typ der **XLOPER12** weist diese Funktion einen neuen Speicherpuffer für die konvertierten Werte zu, auf die im **XlOPER-Zielobjekt verwiesen wird.** Der Aufrufer ist dafür verantwortlich, alle der Kopie zugeordneten Arbeitsspeicher frei zu machen, wenn die Konvertierung erfolgreich war. **FreeXLOperT** kann verwendet werden, oder es kann direkt mithilfe von kostenlos **durchgeführt werden.**
  
Wenn die Konvertierung fehlschlägt, muss der Aufrufer keinen Arbeitsspeicher freispeichern.
  
Die Konvertierung von **einem XLOPER12** in einen **XLOPER** kann fehlschlagen, wenn **xlOPER12** ein Array oder einen Verweis enthält, das zu groß oder eine Zeichenfolge ist, die zu lang ist, damit **xlOPER** enthalten kann. 
  
**XLOPER12** Unicode-Zeichenfolgen mit breiten  Zeichen werden auf eine vom Locale abhängige Weise in XLOPER-ASCII-Bytezeichenfolgen konvertiert. 
  
**XlOPER12** **xltypeInt** ist eine ganzzahlige 32-Bit-Signierte, während **xlOPER** **xltypeInt** eine 16-Bit-ganze Zahl ist. Wenn eine angegebene **XLOPER12-Ganzzahl** den Grenzwert einer **XLOPER-Ganzzahl** überschreitet, wird die ganze Zahl in ein 8-Byte-Double konvertiert und in einem **XLOPER** vom Typ **xltypeNum** zurückgegeben. Dies ist der einzige Fall, in dem diese Funktion den Typ des konvertierten **XLOPER ändert.**
  
### <a name="example"></a>Beispiel

In der Datei  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` finden Sie den Code für diese Funktion. 
  
## <a name="see-also"></a>Siehe auch

- [Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

