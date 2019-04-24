---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- xloper12toxloper-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 148353dcec1cc051aa44d18c0a081b6623e3759a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310073"
---
# <a name="xloper12toxloper"></a>XLOper12ToXLOper

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Konvertierungsroutine, die zum Konvertieren vom neuen **XLOPER12** in den alten **XLOPER**verwendet wird.
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a>Parameter

_pxloper12_ (**LPXLOPER12**)
  
Zeiger auf den zu konvertierenden Quell- **XLOPER12** . 
  
_pxloper_ (**LPXLOPER**)
  
Zeiger auf die Ziel- **XLOPER** , die den konvertierten Wert enthalten soll. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

**True** , wenn die Konvertierung erfolgreich war, andernfalls **false** . 
  
## <a name="remarks"></a>Bemerkungen

Je nach Typ des **XLOPER12**weist diese Funktion einen neuen Speicherpuffer für die konvertierten Werte zu, auf die im Ziel **XLOPER**verwiesen wird. Der Aufrufer ist für das Freigeben von Speicher für die Kopie verantwortlich, wenn die Konvertierung erfolgreich ist; **FreeXLOperT** kann verwendet werden, oder es kann direkt mit **Free**durchgeführt werden.
  
Wenn die Konvertierung fehlschlägt, muss der Aufrufer keinen Arbeitsspeicher freigeben.
  
Die Konvertierung von einer **XLOPER12** in eine **XLOPER** kann fehlschlagen, wenn die **XLOPER12** ein Array oder einen Verweis enthält, das zu lang ist, oder eine Zeichenfolge, die für die **XLOPER** zu lange enthalten ist. 
  
**XLOPER12** Zeichenfolgen mit Unicode-Zeichenfolge werden in **XLOPER** ASCII-Byte Zeichenfolgen in einer gebietsschemaabhängigen Form konvertiert. 
  
**XLOPER12** **xltypeInt** ist eine 32-Bit-Ganzzahl mit Vorzeichen, wohingegen die **XLOPER** - **xltypeInt** eine 16-Bit-Ganzzahl mit Vorzeichen ist. Wenn eine angegebene **XLOPER12** -Ganzzahl den Grenzwert einer **XLOPER** -Ganzzahl überschreitet, wird die ganze Zahl in ein 8-Byte-Double konvertiert und in einer **XLOPER** vom Typ **xltypeNum**zurückgegeben. Dies ist der einzige Fall, in dem diese Funktion den Typ des konvertierten **XLOPER**ändert.
  
### <a name="example"></a>Beispiel

Sehen Sie sich `\SAMPLES\FRAMEWRK\FRAMEWRK.C` die Datei für den Code für diese Funktion an. 
  
## <a name="see-also"></a>Siehe auch

- [Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

