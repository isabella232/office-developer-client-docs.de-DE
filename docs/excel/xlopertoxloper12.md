---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- Xlopertoxloper12-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: b353f32e9bfed784e688f4efcb8969647c279e06
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631419"
---
# <a name="xlopertoxloper12"></a>XLOperToXLOper12

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Konvertierungsroutine, die verwendet wird, um von der alten **XLOPER** in die neue **XLOPER12** zu konvertieren.
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Parameter

_pxloper_ (**LPXLOPER**)
  
Zeiger auf die zu konvertierende **XLOPER-Quelle.** 
  
_pxloper12_ (**LPXLOPER12**)
  
Zeiger auf das **XlOPER12-Ziel,** das den konvertierten Wert enthalten soll. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

**TRUE,** wenn die Konvertierung erfolgreich war, **andernfalls FALSE.** 
  
## <a name="remarks"></a>Bemerkungen

Je nach **XlOPER-Typ** weist diese Funktion einen neuen Speicherpuffer für die konvertierten Werte zu, auf die im **XLOPER12-Ziel** verwiesen wird. Der Aufrufer ist für die Freigabe des Speichers verantwortlich, der der Kopie zugeordnet ist, wenn die Konvertierung erfolgreich ist. **FreeXLOper12T** kann verwendet werden, oder es kann direkt mit **kostenlosen** erfolgen.
  
Wenn die Konvertierung fehlschlägt, muss der Aufrufer keinen Speicher freigeben.
  
Im Allgemeinen ist eine Konvertierung von einem **XLOPER** in ein **XLOPER12** möglich. Im Gegensatz dazu kann die Konvertierung von **XLOPER12** in **XLOPER** fehlschlagen, wenn **XLOPER12** ein Array oder einen Bezug enthält, das zu groß ist, oder eine Zeichenfolge, die zu lang ist, damit **xlOPER** enthalten ist. 
  
**XLOPER** ASCII-Bytezeichenfolgen werden gebietsschemaabhängig in **XLOPER12** Unicode-Breitzeichenzeichenfolgen konvertiert. 
  
### <a name="example"></a>Beispiel

Den Code für diese Funktion finden Sie  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` in der Datei. 
  

