---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- xlgethwnd-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7698404927e11adec70341e791eacf389aafa4f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557603"
---
# <a name="xlgethwnd"></a>xlGetHwnd

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt das Fensterhandle des Fensters der obersten Ebene Microsoft Excel Fensters zurück.
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Enthält das Fensterhandle (**xltypeInt**) im **Feld val.w.** 
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Funktion ist nützlich, um Windows API-Code zu schreiben.
  
Wenn Sie diese Funktion mit [Excel4](excel4-excel12.md) oder [Excel4v](excel4v-excel12v.md)aufrufen, ist die zurückgegebene XLOPER-Ganzzahlvariable eine signierte 16-Bit-Kurzschrift. Dies kann nur die niedrigen 16 Bit des 32-Bit-Windows-Handles enthalten. Um den oberen Teil zu finden, muss Ihr Code alle geöffneten Fenster durchlaufen, um nach einer Übereinstimmung mit dem niedrigen Teil zu suchen. Ab Excel 2007 ist die Ganzzahlvariable von **XLOPER12** ein signiertes 32-Bit-Int und enthält daher das gesamte Handle, sodass alle geöffneten Fenster nicht durchlaufen werden müssen. 
  
### <a name="example"></a>Beispiel

Siehe den Code für die [fShowDialog-Funktion](fshowdialog.md) in  `SAMPLES\GENERIC\GENERIC.C` .
  
## <a name="see-also"></a>Siehe auch

- [xlGetInst](xlgetinst.md)
- [C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

