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
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2c06102699db8810da803ecc0ddfa30375fcc125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790616"
---
# <a name="xloper12toxloper"></a>XLOper12ToXLOper

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Konvertierungsroutine zum Konvertieren von neuen **XLOPER12** in der alten **XLOPER**verwendet.
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a>Parameter

_pxloper12_ (**LPXLOPER12**)
  
Zeiger auf die Quelle **XLOPER12** konvertiert werden soll. 
  
_pxloper_ (**LPXLOPER**)
  
Zeiger auf das Ziel **XLOPER** den konvertierten Wert enthalten. 
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

**True,** Wenn **die Konvertierung erfolgreich; andernfalls** . 
  
## <a name="remarks"></a>Hinweise

Je nach Typ des **XLOPER12**weist diese Funktion einen neuen Speicherpuffer für für die konvertierten Werte, die auf das im Ziel **XLOPER**verwiesen werden. Der Aufrufer ist verantwortlich für das Freigeben von Arbeitsspeicher die Kopie zugeordnet wird, wenn die Konvertierung erfolgreich ist; **FreeXLOperT** kann verwendet werden, oder kann direkt mithilfe von **kostenlose**erfolgen.
  
Wenn die Konvertierung fehlschlägt, muss der Anrufer nicht um Arbeitsspeicher freizugeben.
  
Konvertierung von einem **XLOPER12** in einer **XLOPER** kann misslingen, wenn die **XLOPER12** enthält ein Array oder Verweis, der zu groß ist oder eine Zeichenfolge, die zu lang für die **XLOPER** enthalten ist. 
  
**XLOPER12** Unicode-Breitzeichen-Zeichenfolgen werden in **XLOPER** ASCII-Byte-Zeichenfolgen in einer Weise d. h. Gebietsschema abhängigen konvertiert. 
  
Die **XLOPER12** **vom Typ XltypeInt** ist eine 32-Bit-Ganzzahl mit Vorzeichen, die **XLOPER** **vom Typ XltypeInt** eine 16-Bit-Ganzzahl mit Vorzeichen. Bei einem angegebenen **XLOPER12** Integer ganze **XLOPER** überschreitet, wird die ganze Zahl in eine Double-8-Byte-Wert konvertiert und in ein **XLOPER** des Typs **XltypeNum**zurückgegeben. Dies ist der einzige Fall, in dem diese Funktion den Typ des der konvertierten **XLOPER**ändert.
  
### <a name="example"></a>Beispiel

Finden Sie in der Datei `\SAMPLES\FRAMEWRK\FRAMEWRK.C` für den Code für diese Funktion. 
  
## <a name="see-also"></a>Siehe auch

- [Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

