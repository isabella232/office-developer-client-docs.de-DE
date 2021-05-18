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
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c881f5d03c732b6594e0750808cfa35a65127ed0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404596"
---
# <a name="xlopertoxloper12"></a>XLOperToXLOper12

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Konvertierungsroutine, die zum Konvertieren von der alten **XLOPER** in die neue **XLOPER12 verwendet wird.**
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Parameter

_pxloper_ (**LPXLOPER**)
  
Zeiger auf die zu **konvertierte XLOPER-Quelle.** 
  
_pxloper12_ (**LPXLOPER12**)
  
Zeiger auf das **Ziel XLOPER12,** um den konvertierten Wert zu enthalten. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

**TRUE,** wenn die Konvertierung erfolgreich war, **andernfalls FALSE.** 
  
## <a name="remarks"></a>Hinweise

Je nach Typ der **XLOPER** weist diese Funktion einen neuen Speicherpuffer für die konvertierten Werte zu, auf die im Ziel **XLOPER12 verwiesen wird.** Der Aufrufer ist dafür verantwortlich, alle der Kopie zugeordneten Arbeitsspeicher frei zu machen, wenn die Konvertierung erfolgreich war. **FreeXLOper12T** kann verwendet werden oder direkt mit kostenlosem **.**
  
Wenn die Konvertierung fehlschlägt, muss der Aufrufer keinen Arbeitsspeicher freispeichern.
  
Im Allgemeinen ist eine Konvertierung von **xlOPER** in **xlOPER12** möglich. Im Gegensatz dazu kann die Konvertierung von **xlOPER12** in einen **XLOPER** fehlschlagen, wenn der **XLOPER12** ein Array oder einen Verweis enthält, der zu groß oder eine Zeichenfolge ist, die zu lang ist, damit der **XLOPER** enthalten kann. 
  
**XLOPER** ASCII-Bytezeichenfolgen werden in xlOPER12-Unicode-Breitzeichenzeichenfolgen auf eine vom Locale abhängige Weise konvertiert.  
  
### <a name="example"></a>Beispiel

In der Datei  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` finden Sie den Code für diese Funktion. 
  

