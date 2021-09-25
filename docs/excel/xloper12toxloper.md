---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- Xloper12toxloper-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8d55f9b0dd168725260729ecd61663753ee87a1b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576625"
---
# <a name="xloper12toxloper"></a>XLOper12ToXLOper

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Konvertierungsroutine, die verwendet wird, um von der neuen **XLOPER12** in die alte **XLOPER** zu konvertieren.
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a>Parameter

_pxloper12_ (**LPXLOPER12**)
  
Zeiger auf die zu konvertierende **XLOPER12-Quelle.** 
  
_pxloper_ (**LPXLOPER**)
  
Zeiger auf das **XLOPER-Ziel,** das den konvertierten Wert enthalten soll. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

**TRUE,** wenn die Konvertierung erfolgreich war, **andernfalls FALSE.** 
  
## <a name="remarks"></a>HinwBemerkungeneise

Abhängig vom **XlOPER12-Typ** weist diese Funktion einen neuen Speicherpuffer für die konvertierten Werte zu, auf die im **XLOPER-Ziel** verwiesen wird. Der Aufrufer ist für die Freigabe des Speichers verantwortlich, der der Kopie zugeordnet ist, wenn die Konvertierung erfolgreich ist. **FreeXLOperT** kann verwendet werden, oder es kann direkt **mit** kostenloser .
  
Wenn die Konvertierung fehlschlägt, muss der Aufrufer keinen Speicher freigeben.
  
Die Konvertierung von einem **XLOPER12** in einen **XLOPER** kann fehlschlagen, wenn **XLOPER12** ein Array oder einen Verweis enthält, das zu groß ist, oder eine Zeichenfolge, die zu lang ist, damit **xlOPER** enthalten ist. 
  
**XLOPER12** Unicode-Breitzeichenzeichenfolgen werden gebietsschemaabhängig in **XLOPER** ASCII-Bytezeichenfolgen konvertiert. 
  
**XlOPER12** **xltypeInt** ist eine 32-Bit-Ganzzahl mit Vorzeichen, während **xlOPER** **xltypeInt** eine 16-Bit-Ganzzahl mit Vorzeichen ist. Wenn eine angegebene **XLOPER12-Ganzzahl** den Grenzwert einer **XLOPER-Ganzzahl** überschreitet, wird die ganze Zahl in ein 8-Byte-Double konvertiert und in einem **XLOPER** vom Typ **xltypeNum** zurückgegeben. Dies ist der einzige Fall, in dem diese Funktion den Typ des **konvertierten XLOPER** ändert.
  
### <a name="example"></a>Beispiel

Den Code für diese Funktion finden Sie  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` in der Datei. 
  
## <a name="see-also"></a>Siehe auch

- [Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

