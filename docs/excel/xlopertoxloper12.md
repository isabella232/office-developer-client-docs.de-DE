---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- xlopertoxloper12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: c881f5d03c732b6594e0750808cfa35a65127ed0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303906"
---
# <a name="xlopertoxloper12"></a>XLOperToXLOper12

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Konvertierungsroutine, die zum Konvertieren vom alten **XLOPER** in den neuen **XLOPER12**verwendet wird.
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Parameter

_pxloper_ (**LPXLOPER**)
  
Zeiger auf den zu konvertierenden Quell- **XLOPER** . 
  
_pxloper12_ (**LPXLOPER12**)
  
Zeiger auf die Ziel- **XLOPER12** , die den konvertierten Wert enthalten soll. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

**True** , wenn die Konvertierung erfolgreich war, andernfalls **false** . 
  
## <a name="remarks"></a>Bemerkungen

Je nach Typ des **XLOPER**weist diese Funktion einen neuen Speicherpuffer für die konvertierten Werte zu, auf die im Ziel **XLOPER12**verwiesen wird. Der Aufrufer ist für das Freigeben von Speicher für die Kopie verantwortlich, wenn die Konvertierung erfolgreich ist; **FreeXLOper12T** kann verwendet werden, oder es kann direkt mit **Free**durchgeführt werden.
  
Wenn die Konvertierung fehlschlägt, muss der Aufrufer keinen Arbeitsspeicher freigeben.
  
Im Allgemeinen ist die Konvertierung von einem **XLOPER** in ein **XLOPER12** möglich. Im Gegensatz dazu kann die Konvertierung von einer **XLOPER12** in eine **XLOPER** fehlschlagen, wenn die **XLOPER12** ein Array oder einen Verweis enthält, der zu lang ist, oder eine Zeichenfolge, die zu lange für die **XLOPER** enthalten ist. 
  
**XLOPER** ASCII-Byte Zeichenfolgen werden in **XLOPER12** -Unicode-Breitzeichen Zeichenfolgen in einer gebietsschemaabhängigen Form konvertiert. 
  
### <a name="example"></a>Beispiel

Sehen Sie sich `\SAMPLES\FRAMEWRK\FRAMEWRK.C` die Datei für den Code für diese Funktion an. 
  

