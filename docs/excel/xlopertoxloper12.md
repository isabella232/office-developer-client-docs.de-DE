---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- xlopertoxloper12-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 76c78e5a2ad62b1a3d1aa23748b10e49e07f6543
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790631"
---
# <a name="xlopertoxloper12"></a>XLOperToXLOper12

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Konvertierungsroutine zum Konvertieren von der alten **XLOPER** in die neue **XLOPER12**verwendet.
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Parameter

_pxloper_ (**LPXLOPER**)
  
Zeiger auf die Quelle **XLOPER** konvertiert werden soll. 
  
_pxloper12_ (**LPXLOPER12**)
  
Zeiger auf das Ziel **XLOPER12** den konvertierten Wert enthalten. 
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

**True,** Wenn **die Konvertierung erfolgreich; andernfalls** . 
  
## <a name="remarks"></a>Hinweise

Je nach Typ des der **XLOPER**weist diese Funktion einen neuer Speicherpuffer für die konvertierten Werte, die auf das im Ziel **XLOPER12**verwiesen werden. Der Aufrufer ist verantwortlich für das Freigeben von Arbeitsspeicher die Kopie zugeordnet wird, wenn die Konvertierung erfolgreich ist; **FreeXLOper12T** kann verwendet werden, oder es kann direkt mit **kostenlose**ausgeführt werden.
  
Wenn die Konvertierung fehlschlägt, muss der Anrufer nicht um Arbeitsspeicher freizugeben.
  
Im Allgemeinen ist die Konvertierung von jeder **XLOPER** in einer **XLOPER12** möglich. Im Gegensatz dazu kann Konvertierung von einem **XLOPER12** in einer **XLOPER** misslingen, wenn die **XLOPER12** enthält ein Array oder Verweis, der zu groß ist oder eine Zeichenfolge, die zu lang für die **XLOPER** enthalten ist. 
  
**XLOPER** ASCII-Byte-Zeichenfolgen werden in Unicode **XLOPER12** Breitzeichen-Zeichenfolgen in einer Weise konvertiert, die Gebietsschema abhängig ist. 
  
### <a name="example"></a>Beispiel

Finden Sie in der Datei `\SAMPLES\FRAMEWRK\FRAMEWRK.C` für den Code für diese Funktion. 
  

