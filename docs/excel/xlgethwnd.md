---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- xlGetHwnd-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ab4ac1bc040ef2ea9bca182624111e03722c5200
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425456"
---
# <a name="xlgethwnd"></a>xlGetHwnd

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt das Fensterhandle des Microsoft Excel-Fensters auf oberster Ebene zurück.
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Enthält das Fensterhandle (**xltypeInt**) im Feld **Val. w** . 
  
## <a name="remarks"></a>Bemerkungen

Diese Funktion ist nützlich, um Windows-API-Code zu schreiben.
  
Wenn Sie diese Funktion mit [Excel4](excel4-excel12.md) oder [Excel4v](excel4v-excel12v.md)aufrufen, handelt es sich bei der zurückgegebenen XLOPER-ganzzahligen Variablen um einen signierten 16-Bit-short-int-Wert. Dies kann nur die niedrigen 16 Bits des Windows-Handles von 32-Bit enthalten. Um den hohen Anteil zu ermitteln, muss der Code alle geöffneten Fenster durchlaufen, um eine Übereinstimmung mit dem niedrigen Webpart zu suchen. Beginnend mit Excel 2007 ist die ganzzahlige Variable des **XLOPER12** ein signiertes 32-Bit int und enthält daher das gesamte handle, sodass nicht alle geöffneten Fenster durchlaufen werden müssen. 
  
### <a name="example"></a>Beispiel

Weitere Informationen finden Sie im Code für die `SAMPLES\GENERIC\GENERIC.C`fShowDialog- [Funktion](fshowdialog.md) in.
  
## <a name="see-also"></a>Siehe auch

- [xlGetInst](xlgetinst.md)
- [C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

